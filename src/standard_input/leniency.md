# Leniency

It can make sense to be lenient with your users when interpreting their input.[^idiots]

This means accounting for common mistakes people make like having extra spaces or capitalizing things incorrectly.

For this purpose, methods like `strip` and `equalsIgnoreCase` are useful.

```java,no_run
~Scanner scanner = new Scanner(System.in);
~
~String input(String message) {
~    System.out.print(message);
~    return scanner.nextLine();
~}
~
void main() {
    while (true) {
        String response = input("Answer me: yes or no").strip();
        if (response.equalsIgnoreCase("yes")) {
            System.out.println("aight");
        }
        else if (response.equalsIgnoreCase("no")) {
            System.out.println("cool");
        }
        else {
            System.out.println("try again");
            continue;
        }

        break;
    }
}
```

[^idiots]: People are idiots. Their fingers are fat and their wills are weak.