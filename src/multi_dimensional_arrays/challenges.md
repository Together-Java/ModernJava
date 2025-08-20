# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt




## Challenge 1.

Initialize 10x10 2D array of `int`s by size.
Print every element of this new 2D array.

Will any elements of the outermost array be `null`? 
Write down your guess before making the program.

```java,editable
void main() {
    int[][] xs = /* CODE HERE */
    // CODE HERE
}
```

## Challenge 2.

Print out every character in the 2D array of `char`s. After each
row print a new line.

```java,editable
void main() {
    char[][] picture = new char[][] {
        new char[] { ' ', ' ', ' ', ' ' },
        new char[] { ' ', '*', '*', ' ' },
        new char[] { '\\', ' ', ' ', '/' },
        new char[] { ' ', '-', '-', ' ' }
    };

    // CODE HERE
}
```

## Challenge 3.

"Draw" a smiley face on the "canvas" provided by a 5x5 2D `char` array.

Use similar code as the previous challenge to print it out.

```java,editable
void main() {
    final char[][] picture = new char[5][5];

    // CODE HERE
}
```



## Challenge 4.

Write a method named `winner`. It should take in a 2-dimensional
array of `String`s where each character is either `X`, `O`, or an empty string.
This 2D array represents a [game of Tic-Tac-Toe](https://en.wikipedia.org/wiki/Tic-tac-toe).

If there is a winner of the Tic-Tac-Toe game, it should return `X` or `O` depending on who the winner is.
It should return `null` if nobody won or the game is a tie.

```java
String winner(String[][] ticTacToe) {
    // CODE HERE
}

void main() {
    var winnerA = winner(new String[][] {
        new String[] { "X", "X", "" },
        new String[] { "O", "", "" },
        new String[] { "O", "", "" }
    });

    IO.println(winnerA);

    var winnerB = winner(new String[][] {
        new String[] { "X", "X", "X" },
        new String[] { "O", "O", "X" },
        new String[] { "O", "", "O" }
    });

    IO.println(winnerB);

    var winnerC = winner(new String[][] {
        new String[] { "O", "X", "O" },
        new String[] { "O", "O", "X" },
        new String[] { "O", "X", "O" }
    });

    IO.println(winnerC);
}
```


