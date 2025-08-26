# Reprompting

If you ask someone a yes or no question and they respond with "huh?" you might want to ask them again.

This is a good use case for loops. You ask a question and, if the answer you get is acceptable,
you proceed as normal. If it is not then you loop back and ask again.

```java,no_run
void main() {
    while (true) {
        String response = IO.readln("Answer me: yes or no");
        if (response.equals("yes")) {
            IO.println("okay then!");
        }
        else if (response.equals("no")) {
            IO.println("also fine!");
        }
        else {
            IO.println("Not a valid response");
            // Will go back to the top of the loop
            continue;
        }

        // If a "continue" is not hit, exit the loop
        break;
    }
}
```

If the program would normally crash on unexpected input you can use `try` and `catch` to recover
from this and reprompt the user.

This is applicable to `Integer.parseInt`, `Double.parseDouble`, and any other method that would
throw an exception on unexpected inputs.

```java,no_run
void main() {
    int number;
    while (true) {
        String response = IO.readln("What is your least favorite number? ");
        try {
            // Here Integer.parseInt might throw an exception,
            number = Integer.parseInt(response);
        } catch (RuntimeException e) {
            // If that happens, go up to the top and reprompt
            continue;
        }

        // If a "continue" is not hit, exit the loop
        break;
    }

    IO.println("Your least favorite number is " + number);
}
```