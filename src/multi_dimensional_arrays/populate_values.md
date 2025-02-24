# Populate Values

Once you've created a multi-dimensional array you can use loops
to give initial values to its elements.

Since you will end up nesting these loops, its a good example of a place where you should progress
naming your variables `i -> j -> k`.

```java
// If you prefer true as the default over false
// you need to do that work yourself
boolean[][] booleanField = new boolean[25][25];
for (int i = 0; i < booleanField.length; i++) {
    for (int j = 0; j < booleanField[i].length; j++) {
        booleanField[i][j] = true;
    }
}
```

This is helpful if the default values (`null`, `0`, `false`, etc.) are not what you'd prefer