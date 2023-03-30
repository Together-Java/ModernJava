# Labeled Continue

In the same way a labeled break can break out of a nested loop, a labeled continue
can jump back to the start of a nested loop.

You just write `continue` followed by the label name.

```java
// Will keep going back to the top of the outer loop
outerLoop:
while (true) {
    System.out.println("inside outer loop");
    while (true) {
        System.out.println("inside inner loop");
        continue outerLoop;
    }
}
```
