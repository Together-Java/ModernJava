# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

Edit the following program so that the output is zero.

```java
void main() {
    // Only change this line
    String[] words = { "Sam", "I", "Am" };
    System.out.println(array.length);
}
```

## Challenge 2

Using only `System.out.println` and array accesses,
print `hello world` to the screen.

```java
void main() {
    char[] letters = {
        ' ',
        'h',
        'e',
        'l',
        'o',
        'w',
        'r',
        'd'
    };

    // Your code here
}
```

## Challenge 3

Without editing either the array declaration or the loop at the bottom,
make the output of this program `0`.

```java
void main() {
    final int numbers = { 1, 2, 3, 4 };

    // -----------
    // YOUR CODE HERE


    // -----------
    int total = 0;
    int index = 0;
    while (index < numbers.length) {
        total += numbers[index];
        index += 1;
    }
    System.out.println(total);
}
```

## Challenge 4

Make this program output `bulbasaur` without changing anything
above or below the marked areas.

```java
void main() {
    char[] name = { 'b', 'u', 'l', 'b' };

    // -----------
    // YOUR CODE HERE


    // -----------
    char[] toPrint = name;
    System.out.println(toPrint);
}
```
