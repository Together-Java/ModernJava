# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Write a method named `printSquare` which takes one `int` argument named `size`.

The `size` argument should control how big of a square is output.

```java,editable
// CODE HERE

void main() {
    printSquare(4);
    IO.println();

    printSquare(3);
    IO.println();

    printSquare(2);
    IO.println();

    printSquare(1);
    IO.println();
}
```

## Challenge 2.

What happens if a negative number is given to your `printSquare`?

Make it so that if a negative number is given, it works the same as if a positive number
was given.

```java,editable
// CODE HERE

void main() {
    printSquare(3);
    IO.println();
    printSquare(-3);
    IO.println();

    IO.println();
    printSquare(-2);
    IO.println();
    printSquare(2);
}
```

## Challenge 3.

Write a method with four overloads such that
the code in `main` can run unchanged.

```java,editable
// CODE HERE

void main() {
    f(2);
    f("b");
    f('9');
    f(new String[] { "s" });
}
```

## Challenge 4.

Call the defined methods in a way that outputs "I did it!"

```java,editable
void i() {
    IO.print("I");
}

void did(String what) {
    IO.println("did " + what);
}

void space() {
    IO.print(" ");
}

void main() {
    // Code here
}
```