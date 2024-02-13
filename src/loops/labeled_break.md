# Labeled Break

If you want to break out of a nested loop from one of the inner loops, you can use a "labeled break."

```java
~void main() {
outerLoop:
while (true) {
    while (true) {
        break outerLoop;
    }
}
~}
```

To do this, before your outer while or do-while loop you need to add a "label" followed by a `:`.
A label is an arbitrary name just like a variable's name.

```java,no_run
<LABEL>:
while (<CONDITION>) {
    <CODE HERE>
}
```

```java,no_run
<LABEL>:
do {
    <CODE HERE>
} while (<CONDITION>);
```

Then inside of an inner loop, you just need to write `break` followed by the label name.

```java
~void main() {
int x = 5;
int y = 3;

xLoop:
while (x != 0) {
    while (y != 0) {
        if (x == 2 && y == 2) {
            break xLoop;
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

System.out.println("done.");
~}
```

In this case the `x != 0` loop will be broken out of, not the `y != 0` one.
