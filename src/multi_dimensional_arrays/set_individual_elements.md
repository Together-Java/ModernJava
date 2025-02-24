# Set Individual Elements

You can set the value for elements in a multi-dimensional array the same way
as for one-dimensional arrays, just with an extra `[]` for each extra dimension.

```java
String[][] ticTacToe = {
    { "", "", "" },
    { "", "", "" },
    { "", "", "" }
}

ticTacToe[0][0] = "X";

// The above is a shorthand for this
String[] row = ticTacToe[0];
row[1] = "O";
```
