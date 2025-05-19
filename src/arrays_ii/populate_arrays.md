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
IO.println(letters);
~}
```
