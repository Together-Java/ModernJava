# NaN

There is a special floating point number called `NaN`, which stands for "Not a Number."

You generally only encounter `NaN` as the result of doing something silly like dividing zero by zero.

```java,no_run
double nan = 0.0 / 0.0;
```

`NaN` is not equal to itself.

```java
~void main() {
~double nan = 0.0 / 0.0;
// will be false
boolean equalToItself = nan == nan;

System.out.println(equalToItself);
~}
```

`NaN` is not greater than itself.

```java
~void main() {
~double nan = 0.0 / 0.0;
// will be false
boolean greaterThanItself = nan > nan;

System.out.println(greaterThanItself);
~}
```

`NaN` is not less than itself.

```java
~void main() {
~double nan = 0.0 / 0.0;
// will be false
boolean lessThanItself = nan < nan;

System.out.println(lessThanItself);
~}
```

`NaN` is not greater than, less than, or equal to any number.

```java
~void main() {
~double nan = 0.0 / 0.0;
// will all be false
System.out.println(nan < 5);
System.out.println(nan > 5);
System.out.println(nan == 5);
~}
```

None of this is usually useful, but it is fun to know about.
