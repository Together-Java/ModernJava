# null

There is a special value called `null` which is assignable to most types.

```java
void main() {
    String name = null;
    int[] numbers = null;

    System.out.println(name);
    System.out.println(numbers);
}
```

The only types which `null` cannot be assigned to are `int`, `double`, `char`, and `boolean`.[^aswellas]

```java
void main() {
    // Will not work
    int x = null;
}
```

When something has the value of `null` it represents the absence of a "legitimate" value.

A good example is when a puppy is born. It starts without a name and it is later given a name.
`null` is a way to represent the state of the world in the time before it is named.

```java
void main() {
    // Just born, it has no name
    String puppyName = null;
    System.out.println("At the start, the name is " + puppyName);

    puppyName = "Sally";
    System.out.println("Later it was given the name " + puppyName);
}
```

[^aswellas]: As well as `long`, `short`, `byte`, and `float` but I haven't shown you those yet.
