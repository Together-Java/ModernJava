# Addition

You can add any two `double`s using the `+` operator.

```java
~void main() {
double x = 5.1;
// y will be 14.2
double y = x + 9.1;

System.out.println(y);
~}
```

Because of the previously mentioned inaccuracy, the results of additions might not always be what you expect.

```java
~void main() {
~double x = 5.1;
~// y will be 14.2
~double y = x + 9.1;
// z will be 19.299999999999997
double z = x + y;

System.out.println(z);
~}
```

You can add any `int` to a `double` and the result of any such addition will also be a `double`.

```java
~void main() {
int x = 5;
double y = 4.4;
// z will be 9.4
double z = x + y;

System.out.println(x);
System.out.println(y);
System.out.println(z);
~}
```

Even if the result of such an expression will not have any fractional parts, you cannot directly assign it to an int.

```java,does_not_compile
~void main() {
int x = 5;
double y = 4;
// even though z would be 9, which can be stored in an int
// this will not work. The result of the expression is a double.
int z = x + y;

System.out.println(x);
System.out.println(y);
System.out.println(z);
~}
```
