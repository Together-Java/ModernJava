# Iterate over a String

As was shown with `while` loops, being able to count up and down lets
you iterate over each character in a `String`.

```java
~void main() {
String name = "Lavigne";

for (int index = 0; index < name.length(); index++) {
    IO.println(name.charAt(index));
}
~}
```
