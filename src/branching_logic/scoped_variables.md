# Scoped Variables

If you make a variable declaration inside of an `if` or an `else` block,
that declaration will be "scoped" to the block.

```java
int age = 5;

if (age == 5) {
    int nextAge = age + 1;
    System.out.println(nextAge);
}

// If you uncomment this line, there will be an issue
// `nextAge` is not available to the scope outside of the `if`
// System.out.println(nextAge);
```

This scoping applies even if all branches declare the same variable
within their logic.

```java
int age = 22;

if (age > 25) {
    String message = "You might be able to rent a car";
}
else {
    String message = "You cannot rent a car!";
}

// This will not work, because although `message` is declared
// in all branches, it is not declared in the "outer scope"
System.out.println(message);
```

This is why you will sometimes need to use delayed assignment.