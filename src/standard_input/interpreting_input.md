# Interpreting Input

When you call `input` the human on the other side can type whatever they want.

This means that, depending on the question you asked, you might need to interpret
what they typed as something other than a generic `String`.

In its most basic form this will look like seeing if one `String` equals another `String`.

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
    while (true) {
        String shouldExit = input("Exit the program? (y/n)");
        if (shouldExit.equals("y")) {
            break;
        }
    }
}
```