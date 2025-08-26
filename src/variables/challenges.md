# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

What will this program output when run? Write down your guess and then try running it.

```java,editable
void main() {
    String mascot = "The Noid";
    IO.println(mascot);
    mascot = "Pizza the Hut";
    IO.println(mascot);
    mascot = "Little Caesar";
    IO.println(mascot);
}
```

## Challenge 2

Why won't this code run? Make it run by only changing one line.

```java,editable
void main() {
    String fruit;
    fruit = "apple";

    IO.println(fruit);

    final String vegetable = "carrot";

    IO.println(fruit);
    IO.println(vegetable);

    fruit = "orange";
    vegetable = "celery";

    IO.println(fruit);
    IO.println(vegetable);
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

    IO.println(a);
    IO.println(b);
}
```

<!-- Count not figure out: https://discord.com/channels/272761734820003841/1409741482293858405/1409779369647276074-->
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
    IO.println(a);
    IO.println(b);
}
```

To be clear: you are not allowed to write `b = "A";` or `a = "B";` 

<details>
    <summary> Hint 1: </summary>
    <p> You can always make new variables.</p>
</details>

<details>
    <summary> Hint 2: </summary>
    <p> What you need to do is make a "temporary variable" to hold one of the values before you swap them.</p>
</details>

<details>
    <summary> Solution </summary>
    <p><pre>
String temp = a;
a = b;
b = temp;
</pre></p>
</details>

## Challenge 5

Some of the variables in this program are named "wrong."[^byconvention] Fix them.

```java,editable
void main() {
    String apple = "red";
    String clown_car = "polka dot";
    String SeriousCar = "black";
    String FASTRunner = "bolt";
    String slowRunner = "tortoise";
}
```

[^byconvention]: By currently prevalent social conventions. None are actually "wrong" from the perspective of Java.