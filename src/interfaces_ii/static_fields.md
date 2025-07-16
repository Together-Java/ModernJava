# Static Fields

If there are constants associated with or useful for an interface,
those can be attached to the interface declaration as `public static final` fields.

The declaration of these looks the same as declaring a normal field in a class.
The `public static final` are implied.

```java
interface Biped {
    // This does the same as
    // "public static final int NUMBER_OF_FEET = 2"
    // in a normal class.
    int NUMBER_OF_FEET = 2;

    void walk();
}
```