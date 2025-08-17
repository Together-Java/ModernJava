# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

Make a method named `parseIntChecked` that works the same as `Integer.parseInt`
but throws a checked exception instead of an unchecked one.

```java,editable
// CODE HERE

void main() throws Exception {
    int x = parseIntChecked("45");
    IO.println(x);

    parseIntChecked("abc");
}
```

## Challenge 2

The following program will not compile. Make it compile by propagating the checked exception
thrown by the `doesSomethingDangerous` method.

```java,no_run
int doesSomethingDangerous(int value) {
    if (value == 1) {
        throw new Exception("1 does not work");
    }
    return 3 * value + 2;
}

int compute(int start) {
    return square(doesSomethingDangerous(start));
}

int square(int x) {
    return x * x;
}

void main() {
    int x = Integer.parseInt(IO.readln("Give a starting number: "));
    IO.println(compute(x));
}
```

## Challenge 3

The following program is the same as the last one. Instead of propagating the exception, make it so that 
`compute` catches and rethrows the checked exception as an unchecked one.

```java,no_run
int doesSomethingDangerous(int value) throws Exception {
    if (value == 1) {
        throw new Exception("1 does not work");
    }
    return 3 * value + 2;
}

int compute(int start) {
    return square(doesSomethingDangerous(start));
}

int square(int x) {
    return x * x;
}

void main() {
    int x = Integer.parseInt(IO.readln("Give a starting number: "));
    IO.println(compute(x));
}
```