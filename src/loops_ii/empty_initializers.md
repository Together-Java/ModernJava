# Empty Initializers

You are allowed to leave the initializer part of a `for` loop blank
so long as you still have the `;`.


```java
int number = 0;
for (;number < 5; number++) {
    System.out.println(number);
}
```

You might choose to do this for the same reasons you might choose to split the declaration
and assignment of the "loop variable." 