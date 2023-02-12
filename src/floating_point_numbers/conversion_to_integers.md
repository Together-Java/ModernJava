# Conversion to Integers

Normally, a `double` value cannot be assigned to an `int`.

```java
double x = 5.0;
// will not work
int y = x;
```

The reason for this is that there are numbers like `2.5`, the infinities, and `NaN` which do not have an
obvious way to be represented as an integer. 

There are also numbers which a `double` can represent like `4207483647.0` and `-9999999999.0`
which happen to be too big or too small to fit into the limits of an `int` even though they
do have an obvious "integer representation."

As such, to make an `int` out of a `double` you need to accept that it is a "narrowing conversion."
The number you put in won't neccesarily be the number you get out.

To perform such a narrowing conversion, you need to put `(int)` before a literal or expression that
evaluates to a `double`.

```java
double x = 5.0;
// will be 5
int y = (int) x;

System.out.println(y);
```

Any decimal part of the number will be dropped. So numbers like `2.1`, `2.5`, and `2.9` will all be converted into
simply `2`.

```java
int x = (int) 2.1;
int y = (int) 2.5;
int z = (int) 2.9;

System.out.println(x);
System.out.println(y);
System.out.println(z);
```

Any number that is too big to store in an `int` will be converted to the biggest possible `int`, 2<sup>31</sup> - 1.

```java
// 2147483647
System.out.println((int) 4207483647.0);

double positiveInfinity = 5.0 / 0.0;
// 2147483647
System.out.println((int) positiveInfinity);
```


Any number that is too small to store in an `int` will be converted to the smallest possible `int`, -2<sup>31</sup>.

```java
// -2147483648
System.out.println((int) -9999999999.0);

double negativeInfinity = -5.0 / 0.0;
// -2147483648
System.out.println((int) negativeInfinity);
```

And `NaN` will be converted to zero.

```java
double nan = 0.0 / 0.0;
System.out.println((int) nan);
```

When you use `(int)` to convert, we call that a "cast[^cast] expression". The `(int)` is a "cast operator." It even has 
a place in the operator precedence order just like `+`, `-`, `==`, etc.

The main difference is that instead of appearing between two expressions like the `+` in `2 + 5`, it appears to the left of a single expression.

[^cast]: https://english.stackexchange.com/questions/220001/etymology-of-type-cast