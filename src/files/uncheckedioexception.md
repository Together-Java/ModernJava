# UncheckedIOException

The unchecked version of an `java.io.IOException` is `UncheckedIOException`.

You can use this if you have a method which you don't want to propagate `IOException` but
also want something more specific than `RuntimeException` to re-throw.


And just like `IOException`, if you don't want to write 
out `java.io.UncheckedIOException` more than once you need to add an import.

```java,no_run
import java.io.IOException;
import java.io.UncheckedIOException;

class Main {
    void main() {
        try {
            doStuff();
        }
        catch (IOException e) {
            throw new UncheckedIOException(e);
        }
    }
}
```


```java,does_not_compile
a
b
```


```java,does_not_compile
a
b
c
d
e
f
g
h
i
j
```

```java,panics
a
b
```


```java,panics
a
b
c
d
e
f
g
h
i
j
```

```java,not_desired_behavior
a
b
```


```java,not_desired_behavior
a
b
c
d
e
f
g
h
i
j
```