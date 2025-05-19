# Boolean Expressions

A common thing I've seen students do is set the initial value of some
`boolean` variable based on some condition.

```java
~void main() {
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

IO.println(canRent);
~}
```

This is valid code, but very often can be made simpler if you remember that the condition
itself already evaluates to a `boolean`. You can directly assign the variable to that value.

```java
~void main() {
int age = 22;
boolean canRent = age > 25;

IO.println(canRent);
~}
```
