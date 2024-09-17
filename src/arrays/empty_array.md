# Empty Array

If you use an array initializer that has no elements between the `{` and `}`
you can create an empty array.

```java,no_run
char[] emptyCharArray = {};
```

An empty array is very similar to an empty `String`. It has a length of 0, it has no elements,
and it is generally useful only as a placeholder value for when you have no data yet but will
be able to reassign the variable holding it when you get some.

```java,panics
~void main() {
char[] emptyCharArray = {};

// 0
System.out.println(emptyCharArray.length);

// Crash
System.out.println(emptyCharArray[0]);
~}
```