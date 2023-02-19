# Positive and Negative Infinity

In addition to the wackyness of `NaN`, floating point numbers can also represent both positive
and negative infinity.

You can get positive infinity by dividing any positive number by zero.

```java
double positiveInfinity = 1.0 / 0.0;
```

You can get negative infinity by dividing any negative number by zero.

```java
double negativeInfinity = -1.0 / 0.0;
```

As you might expect, positive infinity is greater than any number and negative infinity is less than any number.

```java
// true
System.out.println(positiveInfinity > 99999999);

// true
System.out.println(negativeInfinity < -99999999);
```

Except for `NaN`, of course.

```java
double nan = 0.0 / 0.0;

// false
System.out.println(positiveInfinity > nan);

// false
System.out.println(negativeInfinity < nan);
```
