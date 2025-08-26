# Purpose

The purpose of streams is to "de-couple"
the source of data, the transformations to apply on that
data, and the final shape you want that data in.

This serves one somewhat holistic goal and one practical one.

The holistic goal is that you are "declaring what you want done"
as opposed to "expressing how you want something done."
This is often referred to as "declarative" vs "imperative" programming.

Compare these two bits of code. They both add one to every number in a list.

```java,no_run
List<Double> doubles = List.of(1.5, 2.5, 3.9);

List<Double> newDoubles = new ArrayList<>();
for (double d : doubles) {
    newDoubles.add(d + 1);
}
```

```java
List<Double> doubles = List.of(1.5, 2.5, 3.9);

List<Double> newDoubles = doubles.stream()
    .map(d -> d + 1)
    .toList();
```

You can argue that the second code snippet more transparently "reflects the intent"
than the first one. The mechanics of looping and adding to a new list are
hidden and the only things on screen are `doubles.stream()` (using this collection as a source),
`.map(d -> d + 1)` (apply this transformation), and `.toList()` (put the results in a list.)

This has its upsides and downsides. Part of the trouble is that there isn't a good rule of
thumb as to when you should use a regular loop or use a stream - it often comes down to
personal taste and other "soft" factors.

The mechanical reason for streams is that, because the operations to perform are separated somewhat
from how to perform them, there are opportunities for Java to be "smart" about how it does them.
The usual example given for this is "parallel streams," which we can get into eventually.