# Array Initializers

To give an initial value to a multi-dimensional array you can use multiple nested
array initializers.

These are the same as normal array initializers but with potentially more initializers inside.[^moray]

```java,no_run
String[][] ticTacToe = {
    { "O", "",  "O" },
    { "X", "O", "X" },
    { "O", "X", "X" }
}
```

[^moray]: When array initizalize and more initialize inside that's a moray.