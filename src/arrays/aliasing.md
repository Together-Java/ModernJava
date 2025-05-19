# Aliasing

When you assign a variable containing an array to another variable, the array
referenced by both variables will be the exact same.

This means that if the contents of the array are updated, that change will
be reflected by both variables.

```java
~void main() {
char[] lettersOne = { 'B', 'a', 't', 'm', 'a', 'n' };
char[] lettersTwo = lettersOne;

// Batman
IO.println(lettersOne);
// Batman
IO.println(lettersTwo);

lettersOne[0] = 'C';

// Catman
IO.println(lettersOne);
// Catman
IO.println(lettersTwo);

lettersTwo[0] = 'R';

// Ratman
IO.println(lettersOne);
// Ratman
IO.println(lettersTwo);
~}
```

When two variables point to the same thing like this we say that both variables are "aliases"
for eachother.
