# Drawing Isosceles Triangles

Another fun shape is the isosceles triangle.

```
  *
 ***
*****
```

For this one, each row of the triangle needs to have spaces before it to shift it in to the
center. How much each row needs to be shifted depends on how big the trangle will be overall.

In this case with three rows of `*`s, the top `*` needs two space characters before it
and the second row needs one space character.

```java
~void main() {
System.out.println("   *\n  ***\n*****");
~}
```

So any loop we make needs to take this pattern into account.

```java
~void main() {
int totalRows = 5;
for (int row = 1; row <= totalRows; row++) {
    for (int i = 0; i < totalRows - row; i++) {
        System.out.print(" ");
    }
    for (int i = 0; i < row * 2 - 1; i++) {
        System.out.print("*");
    }
    System.out.println();
}
~}
```

```
    *
   ***
  *****
 *******
*********
```

Which can get tricky. For now, you can just study the code that does it for this shape. There will be more things to draw
in the challenges section.[^reason]

[^reason]: The reason I'm focusing on this isn't because its likely you will get a job drawing shapes, but if you can draw a shape [you can dodge a ball](https://www.youtube.com/watch?v=1ZXHsNqkDI4).
