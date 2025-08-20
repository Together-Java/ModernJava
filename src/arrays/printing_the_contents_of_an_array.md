# Printing the Contents of an Array

If you try to use `IO.println` to output a `String[]`
you won't see the contents of the array. Instead you will see
something like `[Ljava.lang.String;@1c655221`.

```java
~void main() {
String[] shout = { "fus", "ro", "dah" };
// [Ljava.lang.String;@5a07e868
IO.println(shout);
~}
```

A similar thing will happen with `int[]`, `boolean[]`, and `double[]`.[^gibberish]

```java
~void main() {
int[] nums = { 11, 11, 11 };
// [I@5a07e868
IO.println(nums);

boolean[] bools = { true, false };
// [Z@5a07e868
IO.println(bools);

double[] doubles = { 1.1, 1.1, 1.1 };
// [D@5a07e868
IO.println(bools);
~}
```

If you want to actually see the contents of an array, you should
use a loop.[^future]

```java
~void main() {
String[] factions = { "empire", "stormcloaks", "dragons" };

int index = 0;
while (index < factions.length) {
    IO.println(factions[index]);
    index++;
}
~}
```

[^gibberish]: What `[I@5a07e868` and co. mean isn't really important. Try not to get too distracted by it.

[^future]: Later on, there will be easier ways to do this sort of inspection. This is just the one I can demonstrate now.
