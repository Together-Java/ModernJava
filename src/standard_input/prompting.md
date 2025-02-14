# input

To prompt a user for information you use the `IO.readln` function.

`IO.readln` takes a `String` to output as a prompt. This will
work the same as if the `String` was passed to `IO.print`.

The program will then wait until a human types some text and clicks the enter key.
Whatever they typed will be returned to the program as a `String`.

```java,no_run
void main() {
    String name = IO.scanln("What is your name? ");
    System.out.println("Hello, " + name);
}
```

`readln` stands for "read line." It reads the next line a person types.