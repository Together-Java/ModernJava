# Populate Arrays

If the default value for an array is not valid for what you are doing,
you will need to populate the array with better initial values.

For loops are generally good for this purpose.

```java
~void main() {
char[] letters = new char[26];
for (int i = 0; i < letters.length; i++) {
    letters[i] = (char) ('a' + i);
}
System.out.println(letters);
~}
```

But if you are just writing some value to every index
without any other interesting logic, you can use `Arrays.fill`.

```java
~void main() {
int[] allNines = new int[123];
Arrays.fill(allNines, 9);

for (int i = 0; i < allNines.length; i++) {
    System.out.println(allNines[i]);
}
~}
```

You give that the array and the value to fill it with. In the example above, the array starts
out with everything defaulted to `0` and is then filled with `9`s.
