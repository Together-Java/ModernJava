# IOException

If some code is "doing IO" - by which we mean while it is trying to read some <b>I</b>nput or write some <b>O</b>utput - you should expect it to throw an `IOException`.

This class lives in the `java.io` package so to use it by its simple name you need an import.

```java
import java.io.IOException;

class Main {
    void main() throws IOException {
        throw new IOException("Something went wrong");
    }
}
```

Since reading a file is reading some input and writing to a file is writing some output, this exception is relevant to reading and writing files.