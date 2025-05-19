# Strings

As already shown, you can use a case to match `String` values.

```java
~void main() {
String veggie = "cucumber";
switch (veggie) {
    case "cabbage" -> {
        IO.println("A cabbage");
    }
    case "brussel sprout" -> {
        IO.println("A brussel sprout");
    }
    case "cucumber" -> {
        IO.println("A cucumber");
    }
    default -> {
        IO.println("Other");
    }
}
~}
```