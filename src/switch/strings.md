# Strings

As already shown, you can use a case to match `String` values.

```java
~void main() {
String veggie = "cucumber";
switch (veggie) {
    case "cabbage" -> {
        System.out.println("A cabbage");
    }
    case "brussel sprout" -> {
        System.out.println("A brussel sprout");
    }
    case "cucumber" -> {
        System.out.println("A cucumber");
    }
    default -> {
        System.out.println("Other");
    }
}
~}
```