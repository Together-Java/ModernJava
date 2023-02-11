# Floating Point Literals

In order to write a floating point number in a program, you use a "floating-point literal."

```java
1.5
```

Any number written with a decimal point is a floating point literal.

```java
double pi = 3.14;
```

This includes numbers where a decimal point is written, but there is no fractional part
to the number.

```java
5.0
```

You cannot directly give a value to an integer variable using a floating point literal, even if there is no fractional part to the number.

```java
// this will not work
int x = 5.0;
```

The reverse is possible though. You can give a value to a variable that stores
a floating point number using an integer literal.

```java
double x = 5;
```

