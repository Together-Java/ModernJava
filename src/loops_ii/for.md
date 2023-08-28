# For

The `for` loop is a shortcut to writing a `while` loop which
has distinct steps that

- Declare a variable
- Check that variable to know whether to stop iterating
- Update the variable at the end of each iteration

As with many things, this might be easiest to see by looking at an example.

```java
// Will run 10 times
for (int number = 0; number < 10; number++) {
    System.out.println(number);
}
```

That `for` loop works about the same as this `while` loop.

```java
int number = 0;
while (number < 10) {
    System.out.println(number);

    number++;
}
```
