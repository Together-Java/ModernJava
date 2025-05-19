# Enums

Switches really shine with enums.

For each case label you need to use the name of the variant, not prefixed with
the name of the enum.

```java
enum StopLight {
    RED,
    YELLOW,
    GREEN
}

void main() {
    StopLight light = StopLight.GREEN;
    switch (light) {
        case RED -> {
            IO.println("Stop!");
        }
        case YELLOW -> {
            IO.println("Speed up, coward!");
        }
        case GREEN -> {
            IO.println("Go!");
        }
    }
}
```