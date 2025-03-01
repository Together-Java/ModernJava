# float

What `int` is to `long`, `float` is to `double`. Even the type name `double` implicitly means "double the size of a float." So if you want something half the size of a `double` you can use a `float`. 

To write a float in a program you need to write `f` at the end of the floating
point literal.

```java
~void main() {
float f = 3.5f;
System.out.println(f);
~}
```

This is because Java sees floating point literals without a trailing `f` as representing a `double`.

```java,does_not_compile
~void main() {
float f = 3.5;
System.out.println(f);
~}
```

Conversions from a `double` to a `float` are narrowing and require an explicit cast.
Conversions from a `float` to a `double` are widening and do not require a cast.

```java
~void main() {
double a = 6.5;
// Need a cast
float b = (float) a;
System.out.println(b);

float c = 9.5f;
// Do not need a cast
double d = c;
System.out.println(d);
~}
```

And if you have need of a potentially nullable `float`, `Float` with a capital `F` is the boxed version.

```java
~void main() {
// Can't have a null "float"
// float f = null; 

// But you can have a null "Float"
Float f = null;
System.out.println(f);
~}
```

You will really only want a `float` when you are trying to save space in memory.
Otherwise its best to just use a `double`.

```java,no_run
// This array of 2 floats
float[] floats = { 1.0f, 2.0f };
// Will take up as much space as this
// array with 1 double
double[] oneDouble = { 1.0 };
```