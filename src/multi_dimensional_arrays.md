# Multi-Dimensional Arrays

When you make an array in which each element is itself an array
we call that array of arrays a "multi-dimensional array."

```java
class Main {
    void main() {
        int width = 30;
        int height = 30;
        int[][] pixels = new int[width][height];

        for (int i = 0; i < width; i++) {
            for (int j = 0; j < height; j++) {
                pixels[i][j] = 0;
            }
        }
    }
}
```
