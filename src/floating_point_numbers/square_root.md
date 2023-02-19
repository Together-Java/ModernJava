# Square Root

A relatively common operation to want to perform on floating point numbers
is to find their square root.

You can do this with `Math.sqrt`.

```java
double x = 4;
double y = Math.sqrt(x);

// This will output 2
System.out.println(y);
```

You need to write `Math.sqrt` and then inside of parentheses the expression whose value you want to take the square root of..

```java
double x = 5;
double y = 13;
double z = Math.sqrt(9 * x + y);
 
// This will output 7.615773105863909
System.out.println(z);
```

If you try to take the square root of a negative number, the result will be `NaN`.

```java
// will output NaN
System.out.println(Math.sqrt(-5.2));
```
