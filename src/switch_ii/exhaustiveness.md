# Exhaustiveness

When a switch is used as an expression it needs to be exhaustive.

```java
~void main() {
String name = "bob";

boolean cool = switch (name) {
    case "bob" -> false;
    default -> true;
};

System.out.println(cool);
~}
```

If you attempt to make a non-exhaustive switch expression, Java will not let you.

```java,does_not_compile
~void main() {
String name = "bob";

boolean cool = switch (name) {
    case "bob" -> false;
};

System.out.println(cool);
~}
```
