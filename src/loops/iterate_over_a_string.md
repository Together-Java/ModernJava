# Iterate over a String

This general pattern of counting up and counting down becomes
especially useful when you want to iterate over each character in
a `String`.

```java
~void main() {
String name = "Avril";

int index = 0;
while (index < name.length()) {
    IO.println(name.charAt(index));
    index++;
}
~}
```
