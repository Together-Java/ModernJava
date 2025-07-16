# Initialization with new

Just like for one-dimensional arrays, adding `new` and the type of the array before an initializer
will let you use a multi-dimensional array as an expression or for a delayed assignment.

```java
~void main() {
int[][] numbers;
numbers = new int[25][25];

// I think 25 is my favorite number
int length = (new int[25][25] {}).length;
~}
```