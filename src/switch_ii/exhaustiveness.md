# Exhaustiveness

When a switch is used as an expression it needs to be exhaustive.

```java
~void main() {
String name = "bob";

boolean cool = switch (name) {
    case "bob" -> false;
    default -> true;
};

IO.println(cool);
~}
```

If you attempt to make a non-exhaustive switch expression, Java will not let you.

```java,does_not_compile
~void main() {
String name = "bob";

boolean cool = switch (name) {
    case "bob" -> false;
};

IO.println(cool);
~}
```

Unlike in a switch statement, covering all the enum values in a switch expression
is enough for that switch to be considered exhaustive. You do not need an
extra `default` or `case null`[^reason].

```java,no_run
enum Species {
    ALIEN,
    PREDATOR,
    HUMAN
}

void main() {
    Species species = Species.valueOf(
        IO.readln("What do you see? ").toUpperCase()
    );
    String message = switch (species) {
        case ALIEN -> "Run";
        case PREDATOR -> "Fight Back";
        case HUMAN -> "RUN"
    };

    IO.println(message);
}
```

[^reason]: The nitty gritty of why this is comes down to what Java will do if the code is
run with an unexpected enum variant. With a switch statement the code will just move on and
run none of the switch cases. With a switch expression Java will crash on an unexpected value.
This difference is partially due to the fact that switch statements came first in the language
and switch expressions came later. What a world, huh? 