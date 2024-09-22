# Arrays of Boxed Primitives

If you have an array of the boxed version of a type, that is not
compatible with an array containing the unboxed version and vice-versa.[^interesting]

```java,does_not_compile,no_run
int[] numbersOne = { 1, 2, 3 };
Integer[] numbersTwo = { 4, 5, 6 };

// This line won't work
numbersOne = numbersTwo;
// And neither will this one
numbersTwo = numbersOne;
```

This means that to turn something like a `boolean[]` into a `Boolean[]` or vice-versa, 
you must manually make a new array and copy over elements. Doing this in either
direction will work because boxing and unboxing conversions exist between the primitives
and their boxed variants.

```java
~void main() {
boolean[] yesAndNo = new boolean[] { true, false };

Boolean[] yesAndNoCopy = new Boolean[] { false, false };
for (int i = 0; i < yesAndNo.length; i++) {
    // Here a boxing conversion takes place
    yesAndNoCopy[i] = yesAndNo[i];
}

boolean[] yesAndNoCopyCopy = new boolean[] { false, false };
for (int i = 0; i < yesAndNoCopy.length; i++) {
    // And here an unboxing conversion
    yesAndNoCopyCopy[i] = yesAndNoCopy[i];
}
~}
```




[^interesting]: The reasons for this are deeply interesting and have to do with the nitty gritty of how
Java is actually implemented. It might also change in the future.