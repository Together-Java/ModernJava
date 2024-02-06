# Printing the Contents of an Array

If you try to use `System.out.println` to output a `String[]`
you won't see the contents of the array. Instead you will see
something like `[Ljava.lang.String;@1c655221`.

```java
~void main() {
String[] shout = { "fus", "ro", "dah" };
// [Ljava.lang.String;@5a07e868
System.out.println(shout);
~}
```

A similar thing will happen with `int[]`, `boolean[]`, and `double[]`.[^gibberish]

```java
~void main() {
int[] nums = { 11, 11, 11 };
// [I@5a07e868
System.out.println(nums);

boolean[] bools = { true, false };
// [Z@5a07e868
System.out.println(bools);

double[] doubles = { 1.1, 1.1, 1.1 };
// [D@5a07e868
System.out.println(bools);
~}
```

The only kind of array which will include its contents when printed is a `char[]`.
It will be printed as if it were a `String`.

```java
~void main() {
char[] continent = { 'T', 'a', 'm', 'r', 'i', 'e', 'l' };
// Tamriel
System.out.println(continent);
~}
```

If you want to actually see the contents of an array, you should
use a loop.[^future]

```java
String[] factions = { "empire", "stormcloaks", "dragons" };

int index = 0;
while (index < factions.length) {
    System.out.println(factions[index])
    index++
}
```

[^gibberish]: What `[I@5a07e868` and co. mean isn't really important. Try not to get too distracted by it.
[^future]: Later on, there will be easier ways to do this sort of inspection. This is just the one I can demonstrate now.
