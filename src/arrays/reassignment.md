# Reassignment

The length of an array cannot change, but a variable holding an
array can be reassigned to a new array that has a different length.

```java
String[] words = { 1, 2 };
numbers = { numbers[0], numbers[1], 3 };
```

For the purposes of setting elements, this will be a brand new array.

```java
int[] numbers = { 1, 2 };
int[] numbersTwo = numbers;
numbers = { numbers[0], numbers[1], 3 };

number
```