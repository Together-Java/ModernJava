# Default Methods

Interfaces can specify a `default` implementation
for a method.

```java
interface Dog {
    void bark();

    default void barkLoudly() {
        IO.print("(loudly) ");
        bark();
    }
}
```

Classes which implement interfaces do not need an explicit implementation
for 