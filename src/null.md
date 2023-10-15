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

[^aswellas]: As well as `long`, `short`, `byte`, and `float` but I haven't shown you those yet.
