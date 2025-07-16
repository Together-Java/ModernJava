# short

A `short` represents a signed value between `-32768`
and `32767`. Representing a `short` takes twice as much memory as representing
a `byte` and half as much memory as representing an `int`.

```java
~void main() {
short a = 32767;
IO.println(a);
byte b = -32768;
IO.println(b);
~}
```

Operations like `+` and `*` on a `short` will "promote" the result an `int`
and you will need to cast the result. Going from an `int` to a `short`
is a narrowing conversion.

```java
~void main() {
short a = 5;
short b = 6;
// Need to cast the result to a (byte) again
short c = (short) (a * b);
IO.println(c);
~}
```

Conversely, going from a `short` to an `int` is a widening conversion and you won't
need a cast.

```java
~void main() {
short a = 5;
int a2 = a; // Widening conversion
IO.println(a2);
~}
```


And if you have need of a potentially nullable `short`, `Short` with a capital `S` is the boxed version.

```java
~void main() {
// Can't have a null "short"
// short b = null; 

// But you can have a null "Short"
Short b = null;
IO.println(b);
~}
```


A `short` also takes up exactly as much space as a `char` and converting between the two
is allowed, but will still require an explicit cast in both directions.[^neither]

```java
~void main() {
short s = 50;
char c = (char) s;
s = (short) c;
IO.println(c);
~}
```

You will most often want a `short` when you are trying to save space in memory but
need to represent numbers beyond what a `byte` can represent.[^rare]

```java,no_run
// This array of 2 shorts
short[] shorts = { 1, 2 };

// Will take up as much space as this
// array with 1 int
int[] oneInt = { 1 };

// And as much space as this array with 4 bytes
byte[] bytes = { 1, 2, 3, 4 };
```


[^neither]: These are neither narrowing or widening conversions. Java just makes you put
the cast. One way to view this is that when you go from a `short` to a `char` you've transformed a "number" into a "character." So while no information is lost, what the information "represents" has changed.

[^rare]: As you might suspect, this is more rare than the situations where you would want a `byte`.