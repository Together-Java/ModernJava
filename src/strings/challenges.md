# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

What will this program output when run? Write down your guess and then try running it.

```java,editable
void main() {
    String first = "1";
    String second = "2";
    String result = first + second;

    IO.println(result);
}
```

## Challenge 2

What will this program output when run? Write down your guess and then try running it.

```java,editable
void main() {
    String first = "1";
    int second = 2;

    IO.println(first + second);
}
```


## Challenge 3

What will this program output when run? Write down your guess and then try running it.

```java,editable
void main() {
    char first = 'a';
    String second = "b";
    String third = "ab";

    IO.println((first + second).equals(third));
}
```

## Challenge 4

Make it so this program will output `abc` by only changing one line and
not altering the `println` statement.

Before your change, why did it output `294`?

```java,editable
void main() {
    char a = 'a';
    char b = 'b';
    char c = 'c';
    IO.println(a + b + c);
}
```

## Challenge 5

Without adding any new `println`s,
change one line in this program so that it outputs `racecar`.

Try to find two ways to do that.

```java,editable
void main() {
    String racecar = "racecar";

    int diff = 1;

    int index = 6;

    IO.print(racecar.charAt(index));
    index += diff;
    IO.print(racecar.charAt(index));
    index += diff;
    IO.print(racecar.charAt(index));
    index += diff;
    IO.print(racecar.charAt(index));
    index += diff;
    IO.print(racecar.charAt(index));
    index += diff;
    IO.print(racecar.charAt(index));
    index += diff;
    IO.println(racecar.charAt(index));
}
```

