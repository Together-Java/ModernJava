# Boolean Expressions

A common thing I've seen students do is set the initial value of some
`boolean` variable based on some condition.

```java
int age = 22;

boolean canRent;
if (age > 25) {
    canRent = true;
}
else {
    canRent = false;
}

// or
// boolean canRent = age > 25 ? true : false;

System.out.println(canRent);
```

This is valid code, but very often can be made simpler if you remember that the condition
itself already evaluates to a `boolean`. You can directly assign the variable to that value.

```java
int age = 22;
boolean canRent = age > 25;

System.out.println(canRent);
```

