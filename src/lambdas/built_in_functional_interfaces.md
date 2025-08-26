# Built-In Functional Interfaces

Java comes with many functional interfaces as part of its standard library.

You are under no obligation to use any of these. They are convenient because
they are already at hand, but they tend to have very "generic"
names. It is often better to make your own. That being said:

One functional interface that comes with Java is `Runnable`[^javaone].
This describes a method that takes no arguments and returns no values.

```java,no_run
@FunctionalInterface
public interface Runnable {
    void run();
}
```

Another is `Function`. This is a generic interface that describes
a function taking only one argument. `Function` is notable
in that it is an example of a functional interface that contains
both default methods and static methods.

```java,no_run
@FunctionalInterface
public interface Function<T, R> {
    R apply(T t);

    default <V> Function<V, R> compose(Function<? super V, ? extends T> before) {
        Objects.requireNonNull(before);
        return (V v) -> apply(before.apply(v));
    }

    default <V> Function<T, V> andThen(Function<? super R, ? extends V> after) {
        Objects.requireNonNull(after);
        return (T t) -> after.apply(apply(t));
    }

    static <T> Function<T, T> identity() {
        return t -> t;
    }
}
```

Then there is `Consumer` for something that takes an argument and returns something. `BiFunction`
and `BiConsumer` for things that take two arguments, `Supplier` for something
that takes nothing and returns a value... and so on.

Really the important thing is just to know that some of these exist. There are only
slim benefits to using them over interfaces you make yourself. Lambdas and method
references work the same for everyone.


[^javaone]: I think it is really neat that Runnable came with Java 1.0 - nearly two
decades before lambdas were in the language - and yet works perfectly fine with them.
That's design bay-bee[^powers].

[^powers]: Read that in the Austin Powers voice.