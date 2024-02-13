# Equality

Any two `int`s can be inspected to see if their value is equal by using the `==` operator.

Unlike the previous operators, which all take `int`s and produce `int`s as their result, `==` takes two `int`s
and produces a `boolean` as its result.

```java
~void main() {
// 1 is never equal to 2
// this will be false
boolean universeBroken = 1 == 2;
System.out.println(universeBroken);

int loneliestNumber = 1;
int otherLonelyNumber = 2;

// this will be true
boolean bothLonely = loneliestNumber == (otherLonelyNumber - 1);
System.out.println(bothLonely);
~}
```

It is very important to remember that a single `=` does an assignment. Two equals signs `==` checks for equality.

The opposite check, whether things are not equal, can be done with `!=`.

```java
~void main() {
// 1 is never equal to 2
// this will be true
boolean universeOkay = 1 != 2;
System.out.println(universeOkay);
~}
```
