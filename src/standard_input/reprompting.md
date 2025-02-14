# Reprompting

If you ask someone a yes or no question and they respond with "huh?" you might want to ask them again.

This is a good use case for loops. You ask a question and, if the answer you get is acceptable,
you proceed as normal. If it is not then you loop back and ask again.

```java,no_run
void main() {
    while (true) {
        String response = IO.readln("Answer me: yes or no");
        if (response.equals("yes")) {
            System.out.println("okay then!");
        }
        else if (response.equals("no")) {
            System.out.println("also fine!");
        }
        else {
            System.out.println("Not a valid response");
            // Will go back to the top of the loop
            continue;
        }

        // If a "continue" is not hit, exit the loop
        break;
    }
}
```

