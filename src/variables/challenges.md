# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

What will this program output when run? Write down your guess and then try running it.

```java,editable
void main() {
    String mascot = "The Noid";
    System.out.println(mascot);
    mascot = "Pizza the Hut";
    System.out.println(mascot);
    mascot = "Little Caesar";
    System.out.println(mascot);
}
```

## Challenge 2

Why won't this code run? Make it run by only changing one line.

```java,editable
void main() {
    String fruit;
    fruit = "apple";

    System.out.println(fruit);

    final String vegetable = "carrot";

    System.out.println(fruit);
    System.out.println(vegetable);

    fruit = "orange";
    vegetable = "celery";

    System.out.println(fruit);
    System.out.println(vegetable);
}
```

## Challenge 3

What is the output of this code?

```java,editable
void main() {
    String a = "A";
    String b = "B";

    b = a;
    a = b;
    b = a;
    a = b;

    System.out.println(a);
    System.out.println(b);
}
```

## Challenge 4

Only adding lines in the middle and without writing `"A"` or `"B"` again,
make it so that the output of the program is

```text
B
A
```

```java,editable
void main() {
    String a = "A";
    String b = "B";
    // Don't touch above this

    // You can add code here

    // Don't touch below this
    System.out.println(a);
    System.out.println(b);
}
```


## Challenge 5

Some of the variables in this program are named "wrong." Fix them.

```java,editable
void main() {
    String apple = "red";
    String clown_car = "polka dot";
    String SeriousCar = "black";
    String FASTRunner = "bolt";
    String slowRunner = "tortoise";
}
```