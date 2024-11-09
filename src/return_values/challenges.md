# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Make a method that takes a `String` as an argument and returns an `int`
as a result.

How the value for that int is determined is up to you.

```java,editable
// CODE HERE

void main() {
    int x = process("abc");
    System.out.println("Got " + x);
}
```

## Challenge 2.

Define three methods such that the given main method will run.

```java,editable
// CODE HERE

void main() {
    f(g(h(4), "b"), "e", "s");
}
```

## Challenge 3.

Make the following `multiply` method work for negative numbers.
Do this without simply multiplying using the `*` operator.

```java,editable
int multiply(int x, int y) {
    int total = 0;
    for (int i = 0; i < y; i++) {
        total += x;
    }
    return total;
}

void main() {
    System.out.println(multiply(3, 5));

    // System.out.println(multiply(-5, 5));
    // System.out.println(multiply(-5, -2));
    // System.out.println(multiply(9, -2));
}
```

## Challenge 4.

Define a method, `subtractInt`, which makes the following
code run and produce the "correct" result.

You will need to perform a narrowing conversion.

```java,editable
// CODE HERE

double add(double x, double y) {
    return x + y;
}

double multiply(double x, double y) {
    return x * y;
}

void main() {
    int x = 5;
    int y = 8;
    int z = subtractInt(add(4, 5), mul(4, 2));

    System.out.println(z);
}
```

## Challenge 5.


