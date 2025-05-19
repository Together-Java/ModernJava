# Access Individual Elements

Accessing an element in a multi-dimensional array works the same as
accessing the elements of a one-dimensional array. 

Each time you index into it you will get out another array, so you just keep writing `[]` until
you've drilled down to an individual element.

```java
~void main() {
String[][] ticTacToe = {
    { "O", "",  "O" },
    { "X", "O", "X" },
    { "O", "X", "X" }
}

IO.println(ticTacToe[2][1]);

// This is equivalent to the above
String[] row = ticTacToe[2];
IO.println(row[1]);
~}
```