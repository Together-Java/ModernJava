# Raw Types

If generics are cramping your style, you are
technically allowed to turn them off.

If you make an instance of a generic class without
any `<>` we call that a "raw type."

```java
class Box<T> {
    T data;
}

void main() {
    Box b = new Box();
}
```

When you have a raw type you will see `Object` in any place
you put[^unbounded] a type variable. 

This lets you do whatever you want without the burden of having to make sense to Java.

```java
class Box<T> {
    T data;
}

void main() {
    Box b = new Box();
    b.data = 123;
    b.data = "abc";

    if (b.data instanceof String s) {
        IO.println(s);
    }
}
```

Raw types exist for two basic reasons

1. Every now and then Java isn't smart enough. Trust that there are valid reasons to turn off generics, even if I haven't shown you any yet. Avoid doing so yourself - at least for awhile.
2. Generics weren't always in Java! Classes that later were made generic had to stay compatible with old "raw"
usages somehow.

All that is to say: Be aware raw types exist. Make sure you are always putting `<>` otherwise you are falling 
into that mode. Avoid that mode.


[^unbounded]: An "unbounded" type variable to be exact. We'll visit generic bounds later.