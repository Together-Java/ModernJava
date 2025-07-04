# Subtraction

You can subtract any two `double`s using the `-` operator.

```java
~void main() {
double x = 5.1;
// y will be 4.1
double y = x - 9.2;

System.out.println(x);
System.out.println(y);
~}
```

Because of the previously mentioned inaccuracy, the results of subtractions might not always be what you expect.

```java
~void main() {
~double x = 5.1;
~// y will be -4.1
~double y = x - 9.2;
// z will be -4.199999999999999
double z = y - 0.1;

System.out.println(z);
~}
```

You can subtract any `int` to or from a `double` and the result of any such subtraction will also be a `double`.

```java
~void main() {
int x = 5;
double y = 4.5;
// z will be 0.5
double z = x - y;

System.out.println(x);
System.out.println(y);
System.out.println(z);
~}
```

Even if the result of such an expression will not have any fractional parts, you cannot directly assign it to an `int`.

```java,does_not_compile
~void main() {
int x = 5;
double y = 4;
// even though z would be 1, which can be stored in an int
// this will not work. The result of the expression is a double.
int z = x - y;
~}
```
