# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

Write code that will outputs `The number is even` if `x` is an even number.

```java,editable
void main() {
    // Change this variable to different numbers
    // to test your code
    int x = 5;

    // < YOUR CODE HERE >
}
```

## Challenge 2

Make it so that your code from the previous problem will also output `The number is odd`
if the number is odd.

## Challenge 3

What will this program output when run? Write down your guess and then try running it.

```java,editable
void main() {
  int num = 10;

  if (num > 1)
    IO.println("It is greater than 1");
  if (num > 5)
    IO.println("It is greater than 5");
}
```
<details>
    <summary> Hint 1: </summary>
    <p>Else if statements only execute if previous condition is false.</p>
</details>

<details>
    <summary> Hint 2: </summary>
    <p>If statements always execute.</p>
</details>

<details>
    <summary> Solution </summary>
    <p><pre>
It is greater than 1
It is greater than 5
</pre></p>
</details>

## Challenge 4

Write code that will output `allowed` if the the `password` variable is equal to
`"abc123"` and `not allowed` if it isn't.

```java,editable
void main() {
    // Change this variable to different strings
    // to test your code
    String password = "apple";

    // < YOUR CODE HERE >
}
```

## Challenge 5

Write code that will assign the string `The number {x} is even` to `message` if `x` is an even number
and `The number {x} is odd` if `x` is an odd number.

So if `x` is 12 the string you should assign `The number 12 is even` to `message`.


```java,editable
void main() {
    String message;

    // Change this variable to different numbers
    // to test your code
    int x = 5;

    // < YOUR CODE HERE >

    IO.println(message);
}
```
