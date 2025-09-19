# Iterable and Iterator

For things that are not arrays, a for-each loops
are built on top of two interfaces: `java.lang.Iterable` and `java.lang.Iterator`.

The [`Iterator`](https://docs.oracle.com/en/java/javase/25/docs/api/java.base/java/util/Iterator.html) interface defines two methods: `hasNext` and `next`[^remove]. Iterators let you box up the logic of
how to loop over something.

```java,no_run
public interface Iterator<T> {
    // Will return true if there are more elements
    // false otherwise
    boolean hasNext();

    // Gets an element and advances the iterator forwards
    T next();
}
```

[`Iterable`](https://docs.oracle.com/en/java/javase/25/docs/api/java.base/java/util/Iterable.html) then
just has one method which gives you an `Iterator`. 

```java,no_run
interface Iterable<T> {
    // Gives a "fresh" Iterator
    Iterator<T> iterator();
}
```

This is needed because `Iterator`s are "one shot." It starts at the beginning of a collection
and advances across every element each time `next` is called. In order to loop over something multiple
times you need a fresh iterator each time.  

A for-each loop over an `Iterable` object more or less translates to this style of `while` loop.[^important]

```java,no_run
for (String thing : iterable) {
    // ...
}

// is the same as

Iterator<String> iter = iterable.iterator();
while (iter.hasNext()) {
    String thing = iter.next();
    // ...
}
```


[^remove]: There is actually one more method: `remove`. Not all `Iterator`s support it so we'll cover it once we've introduced more `Iterable` things.

[^important]: I think this is important to know because otherwise it won't make sense when you run in to things you can loop over but don't have `.get`/`[]`, `