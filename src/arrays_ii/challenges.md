# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Make an empty `String` array without using an empty initializer.

This means you cannot write `String[] empty = {}` or `String[] empty = new String[] {}`.

```java,editable
void main() {
    String[] empty = ???;

    // Should be 0
    System.out.println(empty.length);
}
```

## Challenge 2.

What will the following code output? Change the code
between the lines so it instead outputs the following. 

```
1
2
3
4
5
```


```java,editable
void main() {
    Double[] prices = new Double[5];

    // ----------
    // CODE HERE
    // ----------

    for (int i = 0; i < prices.length; i++) {
        double price = prices[i];
        System.out.println(price);
    }
}
```

## Challenge 3.

Only writing code between the lines and without reassigning the `sandwich` variable,
make the following code output `egg and cheese`.

```java,editable
void main() {
    char[] sandwich = new char[14];

    // ----------
    // CODE HERE
    // ----------

    System.out.println(sandwich);
}
```

## Challenge 4.

Populate the `triangle` array such that the code
prints a right triangle that looks like the following.

```
*
**
***
```

```java,editable
void main() {
    char[] triangle = new char[8];

    // ----------
    // CODE HERE
    // ----------

    System.out.println(triangle);
}
```

## Challenge 5.

Make a method named `buildTriangle` which returns a `char[]`
that can be printed out to display a right triangle of any height.

You can ignore the possibility that a negative or zero height is given.

```java,editable
char[] buildTriangle(int height) {
    // CODE HERE
}

void main() {
    System.out.println(buildTriangle(3));
    System.out.println("--------------");
    System.out.println(buildTriangle(5));
    System.out.println("--------------");
    System.out.println(buildTriangle(2));
}
```