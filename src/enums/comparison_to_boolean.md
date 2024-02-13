# Comparison to boolean

Enums are very similar in spirit to `boolean`s.

A `boolean` has one of two values. `true` or `false`.

An enum also has one of a fixed set of values. The difference is that
each item in this fixed set can have its own name and that there might be
more than two values.

Depending on context and personal taste, it might even make sense to use an enum
with two variants as a replacement for a boolean.

```java
enum Power {
    ON,
    OFF
}

void main() {
    Power power = Power.ON;

    if (power == Power.ON) {
        System.out.println("The power is on");
    }
    else {
        System.out.println("The power is off");
    }
}
```

The benefit here being that the names you give to the enum and to the variants
might be clearer to read in code than `boolean`, `true`, and `false`.

The downside being that you needed to write more code.