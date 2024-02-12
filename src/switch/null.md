# null

When a switch is given a `null` value a `NullPointerException` will be thrown immediately.

```java,panics
void eat(String food) {
    switch (food) {
        case "dog food" -> {
            System.out.println("Crunch");
        }
        case "cat food" -> {
            System.out.println("Slorp");
        }
        default -> {
            System.out.println("Other food");
        }
    }
}

void main() {
    eat(null);
}
```

The only exception to this is when a switch has an explcit `case null` in its list of
case labels. `default` will not suffice.

```java
void eat(String food) {
    switch (food) {
        case "dog food" -> {
            System.out.println("Crunch");
        }
        case "cat food" -> {
            System.out.println("Slorp");
        }
        case null -> {
            System.out.println("No food");
        }
        default -> {
            System.out.println("Other food");
        }
    }
}

void main() {
    eat(null);
}
```

A default branch and a null case can be combined by separating them with a comma.

```java
void eat(String food) {
    switch (food) {
        case "dog food" -> {
            System.out.println("Crunch");
        }
        case "cat food" -> {
            System.out.println("Slorp");
        }
        case null, default -> {
            System.out.println("Other food");
        }
    }
}

void main() {
    eat(null);
}
```