# Conversion from Integers

An `int` can represent more values than a `char`, so conversion from `int` to
char requires the use of the cast operator `(char)`.

```java
int x = 120;

char xAsChar = (char) x;

System.out.println(xAsChar);
```

This conversion is narrowing, so information might be lost if the `int` value is too big or too small to fit into a `char`.

The initial value of a `char` can also be given by an integer literal if the integer literal represents a small enough letter.

```java
char z = 122;

System.out.println(z);
```

