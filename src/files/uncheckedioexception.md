# UncheckedIOException

The unchecked version of an `IOException` is `UncheckedIOException`.

You can use this if you have a method which you don't want to propagate `IOException` but
also want something more specific than `RuntimeException` to re-throw.

```java,no_run
void example() {
    try {
        doStuff();
    }
    catch (IOException e) {
        throw new UncheckedIOException(e);
    }
}
```