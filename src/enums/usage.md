# Usage

To use an enum, first make a variable or field whose type is
the name of the enum. Then assign to it one of the variants.

You can access the variants of an enum by writing the enum's name,
a `.`, then the name of the variant.

```java
enum StopLight {
    RED,
    YELLOW,
    GREEN
}

void main() {
    StopLight light = StopLight.RED;

    System.out.println(
        "The light is " + light
    );
}
```