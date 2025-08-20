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
IO.print(lettersOne[0]);
IO.print(lettersOne[1]);
IO.print(lettersOne[2]);
IO.print(lettersOne[3]);
IO.print(lettersOne[4]);
IO.print(lettersOne[5]);
IO.println();
// Batman
IO.print(lettersTwo[0]);
IO.print(lettersTwo[1]);
IO.print(lettersTwo[2]);
IO.print(lettersTwo[3]);
IO.print(lettersTwo[4]);
IO.print(lettersTwo[5]);
IO.println();

lettersOne[0] = 'C';

// Catman
IO.print(lettersOne[0]);
IO.print(lettersOne[1]);
IO.print(lettersOne[2]);
IO.print(lettersOne[3]);
IO.print(lettersOne[4]);
IO.print(lettersOne[5]);
IO.println();
// Catman
IO.print(lettersTwo[0]);
IO.print(lettersTwo[1]);
IO.print(lettersTwo[2]);
IO.print(lettersTwo[3]);
IO.print(lettersTwo[4]);
IO.print(lettersTwo[5]);
IO.println();

lettersTwo[0] = 'R';

// Ratman
IO.print(lettersOne[0]);
IO.print(lettersOne[1]);
IO.print(lettersOne[2]);
IO.print(lettersOne[3]);
IO.print(lettersOne[4]);
IO.print(lettersOne[5]);
IO.println();
// Ratman
IO.print(lettersTwo[0]);
IO.print(lettersTwo[1]);
IO.print(lettersTwo[2]);
IO.print(lettersTwo[3]);
IO.print(lettersTwo[4]);
IO.print(lettersTwo[5]);
IO.println();
~}
```

When two variables point to the same thing like this we say that both variables are "aliases"
for eachother.
