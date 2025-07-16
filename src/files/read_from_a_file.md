# Read from a File

To read a file's contents as a `String` you can use the `readString` static method
from `java.nio.file.Files`.

```java
Path tasksPath = Path.of("tasks.txt");
String tasks = Files.readString(tasksPath);
```

Similarly to `Files.writeString`, this can throw an `IOException` if
something goes wrong[^filenotfound].

This can be dealt with in the same way. Either declare the `IOException` in a `throws`
clause or re-throw an unchecked exception.

```java
import java.nio.file.Files;
import java.nio.file.Path;

class Main {
    void main() throws IOExeption {
        Path tasksPath = Path.of("tasks.txt");
        String tasks = Files.readString(tasksPath);

        IO.println(tasks);
    }
}
```

If you choose to re-throw any `IOException` as an unchecked exception then
it might be helpful to remember that delayed assignment is allowed in that context.[^mostly]

```java
import java.nio.file.Files;
import java.nio.file.Path;

class Main {
    void main() {
        Path tasksPath = Path.of("tasks.txt");

        String tasks;
        try {
            tasks = Files.readString(tasksPath);
        }
        catch (IOException e) {
            throw new UncheckedIOException(e);
        }

        IO.println(tasks);
    }
}
```

[^filenotfound]: Usually we can hand-wave this as "when something goes wrong it throws `IOException`," but this is one of those cases where you might care about what exactly went wrong. Specifically, whether the reason you couldn't read a file because the file wasn't there. We'll use this method as an example when we go deeper into Exceptions
so there will be a chance to talk about that.

[^mostly]: Mostly just because it can let you "shrink the scope" of the try-catch.