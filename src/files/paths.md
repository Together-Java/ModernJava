# Paths

All files and folders on your computer can be located by a "path"
like "`Downloads/movie.mp4`."

To store a path in a Java program we use the `Path` class from the `java.nio.file`[^nio]
package. You create these `Path`s by giving a `String` to the `Path.of`
static method.

```java
import java.nio.file.Path;

class Main {
    void main() {
        Path pathToNotes = Path.of("notes.txt");

        System.out.println(pathToNotes);
    }
}
```

[^nio]: `nio` stands for "new IO." So yes, there was an old IO. We will use that too. Its one of many artifacts from Java's interesting and sordid history. 