# Constructor References

You can make a reference to the constructor
of a class by using `::new`.

```java,no_run
// interface Supplier<T> {
//    T get();
// }

Supplier<ArrayList<String>> listSupplier =
    ArrayList::new;
```

This will try and select a constructor overload that
matches the method expected on the interface.

If you need to pass arguments to the constructor then
you should use a regular lambda.

```java,no_run
Supplier<ArrayList<String>> listSupplier = () -> {
    return new ArrayList<>(10);
};
```