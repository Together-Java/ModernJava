# stream

A Java `Stream` represents a "stream[^flow]"
of elements coming from some "source."

You can stream the elements of a `List`
or `Set` by using the `.stream()` instance method
on each.

```java,no_run
Stream<String> heroes = List.of(
    "Deku", 
    "Explosive Hero: Great Explosion Murder God Dynamight",
    "Froppy"
).stream();

Stream<String> villains = Set.of(
    "All for One",
    "Muscular"
).stream();
```

For arrays there is a static method on `Arrays` which
can stream their contents. You could also first convert the
array to a collection with `Arrays.asList`.

```java,no_run
Stream<String> heroes = Arrays.stream(new String[] {
    "Lin Ling", 
    "Lucky Cyan"
});

Stream<String> villains = Arrays.asList(new String[] {
    "E-Soul"
}).stream();
```

If you legitimately do not have a source collection
you can also create a stream directly with `Stream.of`.

```java,no_run
Stream<Character> letterStream = Stream.of('a', 'b', 'c');
```

[^flow]: In real life a stream flows from some source of water
to some destination. The water can carry rocks and other things
along with it. So that is where the metaphor comes from. Real life streams
carry rocks, Java streams carry chunks of data.