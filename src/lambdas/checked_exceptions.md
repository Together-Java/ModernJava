# Checked Exceptions

One thing that might catch you off guard is how lambdas
and method references interact with checked exceptions.

Normally if the implementation of a functional interface throws
an exception that is allowed.

```java
class Main {
    void main() {
        Function<String, Integer> parseObject 
            = Integer::parseInt;

        int x = parseObject.apply("1657");

        IO.println(x);
    }
}
```

But if the implementation throws a checked exception Java
will complain.

This is because checked exceptions need to be declared in a method signature.
If the functional interface you are making an implementation
does not declare a checked exception is thrown in its single method

```java,does_not_compile
import module java.base;

@FunctionalInterface
interface Loader<T> {
    T load();
}

class Main {
    void main() throws IOException {
        Files.writeString(Path.of("one.txt"), "One and only one");
        // Files.readString can throw an IOException and that is checked
        Loader<String> loader = () -> Files.readString(Path.of("one.txt"));
        IO.println(loader.load());
    }
}
```

One solution is to edit the functional interface such that it declares 
the thrown exception.


```java
import module java.base;

@FunctionalInterface
interface Loader<T> {
    // If we add this throws it will be fine.
    T load() throws IOException;
}

class Main {
    void main() throws IOException {
        Files.writeString(Path.of("one.txt"), "One and only one");
        Loader<String> loader = () -> Files.readString(Path.of("one.txt"));
        IO.println(loader.load());
    }
}
```

The other solution is to catch and rethrow any exceptions as unchecked.


```java,does_not_compile
import module java.base;

@FunctionalInterface
interface Loader<T> {
    T load();
}

class Main {
    void main() throws IOException {
        Files.writeString(Path.of("one.txt"), "One and only one");
        Loader<String> loader = () -> {
            try {
                return Files.readString(Path.of("one.txt"));
            } catch (IOException e) {
                // No issue throwing unchecked exceptions
                throw new UncheckedIOException(e);
            }
        };
        IO.println(loader.load());
    }
}
```

Which of those two solutions you pick will be context dependent.
If you don't control the implementation of the functional interface
(such as with the built-in `Runnable`, `Function`, `Supplier`, etc.)
your best option is the second one.