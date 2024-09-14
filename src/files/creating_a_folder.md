# Creating a Folder

To create a folder, you can use `Files.createDirectory`.

```java
import java.nio.file.Files;
import java.nio.file.Path;

class Main {
    void main() throws IOExeption {
        Path folderPath = Path.of("example1");
        Files.createDirectory(folderPath);
    }
}
```

This, like the other methods in `Files`, might throw an `IOException`.

`Files.createDirectory` will fail if the folder already exists.
