# Challenges

Remember the rules for this are

* Try to use only the information given up to this point in this book.
* Try not to give up until you've given it a solid attempt

## Challenge 1

Write code that will outputs `The number is even` if `x` is an even number.

~IF toplevel_anonymous_class

```java
void main() {
    // Change this variable to different numbers
    // to test your code
    int x = 5;

    // < YOUR CODE HERE >
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        // Change this variable to different numbers
        // to test your code
        int x = 5;

        // < YOUR CODE HERE >
    }
}
```

~ENDIF

## Challenge 2

Make it so that your code from the previous problem will also output `The number is odd`
if the number is odd.

## Challenge 3

Write code that will output `allowed` if the the `password` variable is equal to
`"abc123"` and `not allowed` if it isn't.

~IF toplevel_anonymous_class

```java
void main() {
    // Change this variable to different strings
    // to test your code
    String password = "apple";

    // < YOUR CODE HERE >
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        // Change this variable to different strings
        // to test your code
        String password = "apple";

        // < YOUR CODE HERE >
    }
}
```

~ENDIF

## Challenge 4

Write code that will assign the string `The number is {x} even` to `message` if `x` is an even number
and `The number is {x} odd` if `x` is an even number.

So if `x` is 12 the string you should assign `The number 12 is even` to `message`.

~IF toplevel_anonymous_class

```java
void main() {
    String message;

    // Change this variable to different numbers
    // to test your code
    int x = 5;

    // < YOUR CODE HERE >

    System.out.println(message);
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        String message;

        // Change this variable to different numbers
        // to test your code
        int x = 5;

        // < YOUR CODE HERE >

        System.out.println(message);
    }
}
```

~ENDIF