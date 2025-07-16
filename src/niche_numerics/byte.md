# byte

A `byte` represents a signed value between `-128`
and `127`.

```java
~void main() {
byte a = 127;
IO.println(a);
byte b = -128;
IO.println(b);
~}
```

Operations like `+` and `*` on a `byte` will "promote" the result an `int`
and you will need to cast the result. Going from an `int` to a `byte`
is a narrowing conversion.

```java
~void main() {
byte a = 5;
byte b = 6;
// Need to cast the result to a (byte) again
byte c = (byte) (a * b);
IO.println(c);
~}
```

Conversely, going from a `byte` to an `int` is a widening conversion and you won't
need a cast.

```java
~void main() {
byte a = 5;
int a2 = a; // Widening conversion
IO.println(a2);
~}
```


And if you have need of a potentially nullable `byte`, `Byte` with a capital `B` is the boxed version.

```java
~void main() {
// Can't have a null "byte"
// byte b = null; 

// But you can have a null "Byte"
Byte b = null;
IO.println(b);
~}
```

You will most often want a `byte` when you are trying to save space in memory.

```java,no_run
// This array of 4 bytes
byte[] bytes = { 1, 2, 3, 4 };
// Will take up as much space as this
// array with 1 int
int[] oneInt = { 1 };
```


