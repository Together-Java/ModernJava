# Reassignment

The length of an array cannot change, but a variable holding an
array can be reassigned to a new array that has a different length.

```java
int[] numbers = { 1, 2 };
// 2
System.out.println(numbers.length);

numbers = { numbers[0], numbers[1], 3 };
// 3
System.out.println(numbers.length);
```

This reassignment will not be affect any variables which
are aliases for the variable's old value.

```java
char[] wordOne = { 'g', 'o' };
char[] wordTwo = wordOne;
// go
System.out.println(wordOne);
// go
System.out.println(wordTwo);

wordOne = { wordOne[0], wordOne[1], 's', 'h' };

// gosh
System.out.println(wordOne);
// go
System.out.println(wordTwo);

wordTwo[0] = 'n';

// gosh
System.out.println(wordOne);
// no
System.out.println(wordTwo);

wordOne[0] = 'p';

// posh
System.out.println(wordOne);
// no
System.out.println(wordTwo);
```
