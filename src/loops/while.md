# While

One way to make a loop in code is to use `while`.

```java
int x = 5;
while (x != 0) {
    System.out.println(x);
    x--;
}
```

You write `while` followed by a condition inside of `(` and `)` and some code inside of `{` and `}`.

```java
while (CONDITION) {
    <CODE HERE>
}
```

If the condition evaluates to `true` then the code inside of `{` and `}` will run.
After that code runs, the condition will be evaluated again. If it still evaluates to
`true` then the code `{` and `}` will run again.

This will continue until the code in the condition evaluates to `false`.

```java
int glassesOfMilk = 99;
while (glassesOfMilk > 0) {
    System.out.println(
        glassesOfMilk + " glasses of milk left"
    );

    glassesOfMilk--;
}
```

If a loop is made with `while` we call it a "while loop."[^tortoise]

[^tortoise]: "We called him Tortoise because he taught us." - Lewis Carroll