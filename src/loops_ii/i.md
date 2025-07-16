# i

One thing you will very often see if you read other peoples'
code is that the variable being tracked in a for loop is often called
`i`.

```java
~void main() {
String word = "bird";

for (int i = 0; i < array.length; i++) {
    char letter = word.charAt(i);
    IO.println(letter);
}

// b
// i
// r
// d
~}
```

While usually naming variables with single letters isn't a great idea,
most developers carve out an exception for cases like this. Writing `index` gets
tedious.

Its also helpful to go `i -> j -> k` when you end up nesting `for` loops.[^jindex]

```java
~void main() {
char[] letters = { 'A', 'B', 'C' };
int[] numbers = { 1, 2 };

for (int i = 0; i < letters.length; i++) {
    for (int j = 0; j < numbers.length; j++) {
        IO.print(letters[i]);
        IO.println(numbers[j]);
    }
}

// A1
// A2
// B1
// B2
// C1
// C2
~}
```

Just do not start naming all your variables single letters.

[^jindex]: `j` and `k` standing for jindex an kindex respectfully.
