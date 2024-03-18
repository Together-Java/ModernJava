# Boxing Conversion

If you try to assign to a boxed type like `Integer` from some
code that gives you the unboxed version like `int`, then Java will
automatically do that conversion.[^obvious]

```java, no_run
void main() {
    int x = 5;
    Integer y = x;

    System.out.println(x);
    System.out.println(y);
}
```

[^obvious]: This might feel obvious, but this is one of the few places in Java where the type of something "magically" changes. `int` and `Integer`, `char` and `Character`, etc. *are* different types.