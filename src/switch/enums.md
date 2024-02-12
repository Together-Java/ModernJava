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
            System.out.println("Stop!");
        }
        case YELLOW -> {
            System.out.println("Speed up, coward!");
        }
        case GREEN -> {
            System.out.println("Go!");
        }
    }
}
```