# Initialization with Size

Multi-dimensional arrays are used for representing multi-dimensional things.
These tend to also be large things for which writing out every value in an initializer is impractical.

As such, you can initialize them with only an initial size for each dimension.

```java
// Will make a 2d array of 160x144 booleans
boolean[][] pixels = new boolean[160][144];
```
