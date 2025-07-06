# Reassignment

The length of an array cannot change, but a variable holding an
array can be reassigned to a new array that has a different length.

When reassigning the value of an array variable you need to put `new` followed by a space, the type
of element held by the array, and then `[]` all before the initializer.

So to reassign an `int[]` you need to write something like `new int[] { 1, 2, 3 }`.

```java
~void main() {
int[] numbers = { 1, 2 };
// 2
System.out.println(numbers.length);

numbers = new int[] { numbers[0], numbers[1], 3 };
// 3
System.out.println(numbers.length);
~}
```

This reassignment will not affect any variables which
are aliases for the variable's old value.

```java
~void main() {
char[] wordOne = { 'g', 'o' };
char[] wordTwo = wordOne;
// go
System.out.println(wordOne);
// go
System.out.println(wordTwo);

wordOne = new char[] { wordOne[0], wordOne[1], 's', 'h' };

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
~}
```
