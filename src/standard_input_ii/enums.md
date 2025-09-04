# Enums

Just as you might want to interpret what someone typed as an `int` or `double`
there are times you will want to interpret input as an `enum` value.

To do this you can write `.valueOf` after the name of the enum. So for a `StopLight` enum `StopLight.valueOf`
can interpret a `String` as a `StopLight`.

```java,no_run
enum StopLight {
    RED,
    YELLOW,
    GREEN
}

void main() {
    String colorString = IO.readln("What color was the stoplight? ");
    StopLight color = StopLight.valueOf(colorString);
    IO.println("The stop light was " + color);
}
```

This will throw an exception if the `String` does not match, so you can reprompt using the same `try`/`catch` structure as you would use with `Integer.parseInt`.

```java,no_run
enum StopLight {
    RED,
    YELLOW,
    GREEN
}

void main() {
    StopLight color;
    while (true) {
        String colorString = IO.readln("What color was the stoplight? ");
        try {
            color = StopLight.valueOf(colorString);
        } catch (RuntimeException e) {
            continue;
        }

        break;
    }

    IO.println("The stop light was " + color);
}
```

Unfortunately, this only works if what they typed is exactly the name of an enum variant. So 
in the example above they need to type `RED` in all capital letters.

To have a different mapping of strings to enum values you need to write code yourself.

```java,no_run
enum StopLight {
    RED,
    YELLOW,
    GREEN
}

StopLight stringToStopLight(String s) {
    if (s.equals("r")) {
        return StopLight.RED;
    }
    else if (s.equals("y")) {
        return StopLight.YELLOW;
    }
    else if (s.equals("g")) {
        return StopLight.GREEN;
    }
    else {
        throw new RuntimeException("Unknown color.")
    }
}

void main() {
    String colorString = IO.readln("What color was the stoplight? ");
    StopLight color = stringToStopLight(colorString);
    IO.println("The stop light was " + color);
}
```

