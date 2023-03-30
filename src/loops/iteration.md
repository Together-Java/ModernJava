# Iteration

Loops potentially run code multiple times. Each time one goes from its top to its bottom
we call that an "iteration" of the loop.

```java
int x = 0;
while (x < 5) {
    // On the 1st iteration x will be 0
    // On the 2nd iteration x will be 1
    // ...
    // On the final iteration x will be 4
    System.out.println(x);
    x++
}
```

When the purpose of a loop is to run for every thing in some sequence of things,
we say that the loop is "iterating over" those things.
