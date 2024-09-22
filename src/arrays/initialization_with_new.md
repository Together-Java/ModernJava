# Initialization with new

Before the initializer for an array, you are allowed to write
`new` followed by a space, the type of thing in the array,
and an empty `[]`.

```java
~void main() {
char[] mainCharacter = { 'A', 'a', 'n', 'g' };
System.out.println(mainCharacter);

char[] sideCharacter = new char[] { 'A', 'a', 'n', 'g' };
System.out.println(sideCharacter);
~}
```

This is required for performing delayed initialization of a variable
holding an array.

```java
~void main() {
char[] element;

element = new char[] { 'f', 'i', 'r', 'e' };
System.out.println(element);

// This would not work
// element = { 'f', 'i', 'r', 'e' };
~}
```

One ability this gives you is to use an array in an expression. I.E.
the initializer coupled with the `new char[]` is akin to an "array expression."

```java
~void main() {
System.out.println(new char[]{ 'K', 'a', 't', 'a', 'r', 'a' }[1]);
~}
```