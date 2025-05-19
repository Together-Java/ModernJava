# null

When a switch is given a `null` value a `NullPointerException` will be thrown immediately.

```java,panics
void eat(String food) {
    switch (food) {
        case "dog food" -> {
            IO.println("Crunch");
        }
        case "cat food" -> {
            IO.println("Slorp");
        }
        default -> {
            IO.println("Other food");
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
            IO.println("Crunch");
        }
        case "cat food" -> {
            IO.println("Slorp");
        }
        case null -> {
            IO.println("No food");
        }
        default -> {
            IO.println("Other food");
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
            IO.println("Crunch");
        }
        case "cat food" -> {
            IO.println("Slorp");
        }
        case null, default -> {
            IO.println("Other food");
        }
    }
}

void main() {
    eat(null);
}
```