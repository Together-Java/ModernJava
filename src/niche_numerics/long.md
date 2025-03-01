# long

If an `int` is not big enough for your needs, a `long` is twice as big as an `int`
and can represent numbers from `-2^63` to `2^63 - 1`.

You can make a `long` from an integer literal, but integer literals do not
normally allow for numbers that an `int` cannot store. 

```java,does_not_compile
~void main() {
// Smaller numbers work without issue
long smallNumber = 5;
System.out.println(smallNumber);
// This is too big for an int
long bigNumber = 55555555555;
System.out.println(bigNumber);
~}
```

For those cases you need to add an `L` to the end of the literal.[^lforlong]

```java
~void main() {
long smallNumber = 5;
System.out.println(smallNumber);
// But with an L at the end, its not too big for a long
long bigNumber = 55555555555L;
System.out.println(bigNumber);
~}
```

All operations with a `long` will result in a `long`. Conversions to `int` and
other "smaller" integer types will be narrowing and require a cast.

```java
~void main() {
long a = 5;
int b = 3;
// a long times an int will result in a long
long c = a * b;
System.out.println(c);
~}
```

And if you have need of a potentially nullable `long`, `Long` with a capital `L` is the boxed version.

```java
~void main() {
// Can't have a null "long"
// long l = null; 

// But you can have a null "Long"
Long l = null;
System.out.println(l);
~}
```

The reason you will likely end up using `int` more than `long` is that `int`
works more with other parts of Java. Like array indexing - you can't
get an item in an array with a `long`, you need an `int` for that.

```java,does_not_compile
~void main() {
String[] sadRobots = { "2B", "9S", "A2" };
long index = 2;
// Longs can't be used as indexes
String sadRobot = sadRobots[index];
~}
```

But there is nothing wrong with a `long`. If you need to represent a number that is potentially bigger than an `int` then it is useful.


[^lforlong]: "L is for long" would be a total cop-out in a children's picture book.