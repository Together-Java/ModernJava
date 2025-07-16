# StringBuilder

`String`s cannot be changed in place. This means that every operation
on a `String` needs to produce a brand new `String` as a result.

Normally this is fine, but when you do something like that in a loop
it can become a performance problem.

```java
String removeAllNumbers(String input) {
    String result = "";
    for (int i = 0; i < input.length(); i++) {
        char c = input.charAt(i);
        if (c < '0' || c > '9') {
            result = result + c;
        }
    }
    return result;
}

void main() {
    String screenplay = "5".repeat(1000000);
    // There are 1301 characters in the above text, meaning this method
    // does around that many copies of the string
    IO.println(removeAllNumbers(screenplay));
}
```

```java
String removeAllNumbers(String input) {
    StringBuilder result = new StringBuilder();
    for (int i = 0; i < input.length(); i++) {
        char c = input.charAt(i);
        if (c < '0' || c > '9') {
            result.append(c);
        }
    }
    return result.toString();
}

void main() {
    String screenplay = "5".repeat(1000000);
    // There are 1301 characters in the above text, meaning this method
    // does around that many copies of the string
    IO.println(removeAllNumbers(screenplay));
}
```