# IOException

If some code is "doing IO" - by which we mean while it is trying to read some <b>I</b>nput or write some <b>O</b>utput - you should expect it to throw an `IOException`.[^isa]

```java
void main() throws IOException {
    throw new IOException("Something went wrong");
}
```

For now you just need to know that `IOException` exists. We will encounter it when reading and writing files.

[^isa]: Technically an `IOException` *is* an `Exception`, but we're not quite ready to talk about "exception hierarchies" yet. Hold tight.