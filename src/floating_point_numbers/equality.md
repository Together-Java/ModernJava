# Equality

Just like `int`s, `double`s can be inspected to see if they are equal to one another using `==`.

```java
~void main() {
double numberOfToes = 10.0;
double numberOfFingers = 10.0;

boolean humanGenerated = numberOfToes == numberOfFingers;

System.out.println(humanGenerated);
~}
```

Because of floating point inaccuracy, this might not always give you the result you expect though.

```java
~void main() {
double x = 0.1;
double y = 0.2;
// z will be 0.30000000000000004
double z = x + y;

// this will be false.
boolean doesWhatYouExpect = z == 0.3;

System.out.println(doesWhatYouExpect);
~}
```

A `double` can also be compared to an `int` and, if they represent the same value, they will be reported as equal.

```java
~void main() {
int x = 5;
double y = 5.0;

// will be true
boolean fiveIsFive = x == y;

System.out.println(fiveIsFive);
~}
```
