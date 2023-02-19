# Reassignment

When the value of a variable is reassigned, the value stored in the variable
before the reassignment can be used to compute the new value.

This is true for all data types, but it is easiest to demonstrate with numbers.

```java
int x = 1;
System.out.println(x);

// x starts as 1, 1 + 1 is 2.
// 2 is the new value of x. 
x = x + 1;
System.out.println(x);

// x is now 2, 2 * 2 * 3 is 12
// 12 is the new value of x.
x = x * x * 3;
System.out.println(x);
```

This property was used in the previous example for the `%` operator, but I think it worth calling attention to even if it is "intuitive".
