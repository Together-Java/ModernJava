# Nested Loops

Just like with `if`, The code inside of the `{` and `}` can be anything, including more loops.

```java
~void main() {
int x = 5;
int y = 3;

while (x != 0) {
    while (y != 0) {
        System.out.println(
            "x is " + x
        );
        System.out.println(
            "y is " + y
        );

        x--;
        y--;
    }
}
~}
```

If you are inside such a "nested loop", `continue` and `break` apply to the
"closest" loop.

That is, if a `continue` or a `break` were to appear here

```java
~void main() {
while (x != 0) {
    while (y != 0) {
        if (y == 2) {
            break;
        }

        System.out.println(
            "x is " + x
        );
        System.out.println(
            "y is " + y
        );

        x--;
        y--;
    }
}
~}
```

Then the `y != 0` loop will be broken out of, not the `x != 0` one.
And if a `continue` or a `break` were to appear here

```java
~void main() {
while (x != 0) {
    if (x == 2) {
        break;
    }
    while (y != 0) {


        System.out.println(
            "x is " + x
        );
        System.out.println(
            "y is " + y
        );

        x--;
        y--;
    }
}
~}
```

Then the `x != 0` loop would be the "target."
