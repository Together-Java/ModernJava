# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

What will this program output when run? Write down your guess and then try running it.

```java,editable
void main() {
    int x = 5;
    int y = 8;
    System.out.println(x + y);
}
```

## Challenge 2

What will this program output when run? Write down your guess and then try running it.

```java,editable
void main() {
    int x = 5;
    x--;
    x--;
    x = x + x;
    System.out.println(x);
}
```

## Challenge 3

Make it so that this program correctly determines if the numbers are even or not.

Assume that the values of `x`, `y`, and `z` could be changed. Don't just write out
literally `true` and `false` for their current values.

```java,editable
void main() {
    int x = 5;
    int y = 4;
    int z = 98;

    boolean xIsEven = < CODE HERE >;
    System.out.println(xIsEven);

    boolean yIsEven = < CODE HERE >;
    System.out.println(yIsEven);

    boolean zIsEven = < CODE HERE >;
    System.out.println(zIsEven);
}
```

## Challenge 4

Try dividing a number by zero. What happens?

Write down your guess and then try running the program below to see.

```java,editable
void main() {
    System.out.println(5 / 0);
}
```

## Challenge 5

What can you write in the spot marked that will make the program output 2?

```java,editable
void main() {
    int x = 5;
    int y = <CODE HERE>;
    System.out.println(x + y);
}
```

## Challenge 6

What is the output of this code.[^fbarticle]

```java,editable
void main() {
    System.out.println(
        6 / 2 * (1 + 2)
    );
}
```

[^fbarticle]: [Now get in a fight with your relatives about it](https://slate.com/technology/2013/03/facebook-math-problem-why-pemdas-doesnt-always-give-a-clear-answer.html)
