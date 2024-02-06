# Break

While loops will usually stop running when the condition at the top evaluates
to `false`.

This can be bypassed by using the `break` statement.

```java
~void main() {
int x = 5;
while (x > 0) {
    if (x == 2) {
        break;
    }
    x--;
}

System.out.println(
    "Final value of x is " + x
);
~}
```

If a `break` is reached, the code in the loop stops running immediately.
The condition of the loop is not checked again.

This can be useful in a variety of situations, but notably it is the only way to exit
from an otherwise endless loop.

```java
~void main() {
while (true) {
    System.out.println(
        "The people started singing it not knowing what it was"
    );

    // Will immediately leave the loop
    break;
}
~}
```
