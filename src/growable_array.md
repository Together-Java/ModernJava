# Growable Arrays

Arrays are fixed size collections of elements. This means when we make an array
that is 5 elements big it will always be 5 elements big.

```java
~void main() {
int[] numbers = new int[5];
~}
```

Something that turns out to be extremely useful is to have something with most of the properties of an array - such as being able quickly get and set arbitrary elements by index - but that can grow over time.

The rest of this section I will walk you through how we can accomplish that.

