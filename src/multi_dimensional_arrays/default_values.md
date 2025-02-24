# Default Values

When a multi-dimensional array is made by just providing a size, its elements
are initialized to the same default values as they would be in a regular array.

The difference is that each "nested array" will not be initialized to null.

```java
~void main() {
String[][] ticTacToe = new String[3][3];

// Each array will be non-null
System.out.println(ticTacToe[0]);

// But the elements of those arrays will be null
// (or whatever the default value is for the type.)
System.out.println(ticTacToe[0][0]);
~}
```