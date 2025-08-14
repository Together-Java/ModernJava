# Interpreting Input

When you call `IO.readln` the human on the other side can type whatever they want.

This means that, depending on the question you asked, you might need to interpret
what they typed as something other than a generic `String`.

In its most basic form this will look like seeing if one `String` equals another `String`.

```java,no_run
void main() {
    while (true) {
        String shouldExit = IO.readln("Exit the program? (y/n)");
        if (shouldExit.equals("y")) {
            break;
        }
    }
}
```