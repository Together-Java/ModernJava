# Default Values

When an array is made by just providing a size, its elements
are initialized to some default value.

For primitive types like `int` and `double`, each element will be initialized to `0`.

```java
~void main() {
int[] digits = new int[10];
// 0
System.out.println(digits[0]);

double[] readings = new double[5];
// 0.0
System.out.println(readings[0]);
~}
```

For `boolean`, each element will be initialized to `false`.[^funfact]

```java
~void main() {
boolean[] pokedex = new boolean[10];
// false
System.out.println(pokedex[0]);
~}
```

And for every non-primitive type, which is every single type including the boxed primitives,
the default value will be `null`.

```java
~void main() {
String[] names = new String[10];
// null
System.out.println(names[0]);

Integer[] scores = new Integer[26];
// null
System.out.println(scores[0]);
~}
```

[^funfact]: Fun fact. The GameBoy and GameBoy Advance Pokemon games tracked pokedex completion in a big `boolean` array. If you saw a Pokemon it would flip that Pokemon's index in the "seen" array to `true`. If you caught it, it would do the same in a different array. Those games weren't written in Java, but the concept is the same.