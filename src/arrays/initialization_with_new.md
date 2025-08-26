# Initialization with new

Before the initializer for an array, you are allowed to write
`new` followed by a space, the type of thing in the array,
and an empty `[]`.

```java
~void main() {
char[] mainCharacter = { 'A', 'a', 'n', 'g' };
IO.println(mainCharacter[0]);
IO.println(mainCharacter[1]);
IO.println(mainCharacter[2]);
IO.println(mainCharacter[3]);
IO.println();

char[] sideCharacter = new char[] { 'A', 'a', 'n', 'g' };
IO.println(sideCharacter[0]);
IO.println(sideCharacter[1]);
IO.println(sideCharacter[2]);
IO.println(sideCharacter[3]);
IO.println();
~}
```

This is required for performing delayed initialization of a variable
holding an array.

```java
~void main() {
char[] element;

element = new char[] { 'f', 'i', 'r', 'e' };
IO.println(element[0]);
IO.println(element[1]);
IO.println(element[2]);
IO.println(element[3]);
IO.println();

// This would not work
// element = { 'f', 'i', 'r', 'e' };
~}
```

One ability this gives you is to use an array in an expression. I.E.
the initializer coupled with the `new char[]` is akin to an "array expression."

```java
~void main() {
IO.println(new char[]{ 'K', 'a', 't', 'a', 'r', 'a' }[1]);
~}
```