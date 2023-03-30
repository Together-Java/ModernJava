# Aliasing

When you assign a variable containing an array to another variable, the array
referenced by both variables will be the exact same.

This means that if the contents of the array are updated, that change will
be reflected by both variables.

```java
char[] lettersOne = { 'B', 'a', 't', 'm', 'a', 'n' };
char[] lettersTwo = lettersOne;

// Batman
System.out.println(lettersOne);
// Batman
System.out.println(lettersTwo);

lettersOne[0] = 'C';

// Catman
System.out.println(lettersOne);
// Catman
System.out.println(lettersTwo);

lettersTwo[0] = 'R';

// Ratman
System.out.println(lettersOne);
// Ratman
System.out.println(lettersTwo);
```

When two variables point to the same thing like this we say that both variables are "aliases"
for eachother.
