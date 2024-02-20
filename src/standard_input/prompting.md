# input

To prompt a user for information you use the `input` function.

The `input` function takes a `String` to output as a prompt. This will
work the same as if the `String` was passed to `System.out.print`.

The program will then wait until a human types some text and clicks the enter key.
Whatever they typed will be returned to the program as a `String`.

```java,no_run
~import java.util.Scanner;
~
~Scanner scanner = new Scanner(System.in);
~
~String input(String message) {
~    System.out.print(message);
~    return scanner.nextLine();
~}
~
void main() {
    String name = input("What is your name? ");
    System.out.println("Hello, " + name);
}
```