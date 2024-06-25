# Write to a File

To write a `String` to a file you can use the `Files` class from the `java.nio.file`
package. It has a static method named `writeString`.

```java,no_run
Path tasksPath = Path.of("tasks.txt");
String tasks = """
    1. Do dishes
    2. Do laundry
    """;

Files.writeString(tasksPath, tasks);
```

This method can throw an `IOException`, so to handle that you
can have a `throws` declaration on the method calling it.

```java,no_run
import java.nio.file.Files;
import java.nio.file.Path;

class Main {
    void main() throws IOException {
        Path tasksPath = Path.of("tasks.txt");
        String tasks = """
            1. Do dishes
            2. Do laundry
            """;

        Files.writeString(tasksPath, tasks);
    }
}
```

The other option is to catch the `IOException` and re-throw it as an unchecked exception.

```java,no_run
import java.nio.file.Files;
import java.nio.file.Path;

class Main {
    void main() {
        Path tasksPath = Path.of("tasks.txt");
        String tasks = """
            1. Do dishes
            2. Do laundry
            """;

        try {
            Files.writeString(tasksPath, tasks);
        }
        catch (IOException e) {
            throw new UncheckedIOException(e);
        }    
    }
}
```