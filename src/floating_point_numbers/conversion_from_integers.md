# Conversion from Integers

To convert from an `int` to a `double`, you don't need to do any special work. All `int`s are
representable as `double`s so it is a "widening conversion" and will be handled automatically
by the language when performing an assignment.

```java
int x = 5;
double y = x;

System.out.println(x);
System.out.println(y);
```

This is not true in an expression. Even if the result of a computation between `int`s is being assigned to
a `double`, the computation will still be performed using the same rules `int`s usually follow.

```java
int x = 7;
int y = 2;
// integer division of 7 and 2 gives 3.
double z = x / y;

System.out.println(z);
```

To perform math on an `int` and have that `int` behave as if it were a `double`, you need to convert said `int` into
a `double` using a cast expression and the `(double)` cast operator.

```java
int x = 7;
int y = 2;
// This converts x into a double before performing the division
// so the result will be 3.5.
double z = (double) x / y;

System.out.println(z);
```

