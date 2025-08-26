# Leniency

It can make sense to be lenient with your users when interpreting their input.[^idiots]

This means accounting for common mistakes people make like having extra spaces or capitalizing things incorrectly.

For this purpose, methods like `strip` and `equalsIgnoreCase` are useful.

```java,no_run
void main() {
    while (true) {
        String response = IO.readln("Answer me: yes or no").strip();
        if (response.equalsIgnoreCase("yes")) {
            IO.println("aight");
        }
        else if (response.equalsIgnoreCase("no")) {
            IO.println("cool");
        }
        else {
            IO.println("try again");
            continue;
        }

        break;
    }
}
```

[^idiots]: People are idiots. Their fingers are fat and their wills are weak.