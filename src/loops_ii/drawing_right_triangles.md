# Drawing Right Triangles

One of the more fun things to do with `for` loops[^quiz] is to use them to print out shapes.

Say you wanted to draw this right triangle.

```
*
**
***
```

There is one `*`, then two `*`s on the next line, and three `*`s on the last.

If you were to write the code out to print this explicitly it would look like this.

```java
~void main() {
IO.print("*\n**\n**\n");
~}
```

Where `\n` is explicitly putting in the new lines.

Since counting up `1 -> 2 -> 3` is easy with `for` loops, you can translate this

```java
~void main() {
for (int numberOfStars = 1; numberOfStars <= 3; numberOfStars++) {
    for (int i = 0; i < numberOfStars; i++) {
        IO.print("*");
    }
    // Same as IO.print("\n");
    IO.println();
}
~}
```

Which makes it easy to make one of these triangles however tall you want.

```java
~void main() {
int height = 6;
for (int numberOfStars = 1; numberOfStars <= height; numberOfStars++) {
    for (int i = 0; i < numberOfStars; i++) {
        IO.print("*");
    }
    IO.println();
}
~}
```

```
*
**
***
****
*****
******
```
