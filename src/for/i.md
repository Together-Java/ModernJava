# i

One thing you will very often see if you read other peoples'
code is that the variable being tracked in a for loop is often called
`i`.

```java
String word = "bird";
for (int i = 0; i < array.length; i++) {
    char letter = word.charAt(i);
    System.out.println(letter);
}

// b
// i
// r
// d
```

While usually naming variables with single letters isn't a great idea,
most developers carve out an exception for cases like this.

If a for loop that starts its variable at `0`, keeps going until while
it is `<` the length of some collection, and goes up by one each iteration
it should be "obvious" what `i` means.

Just do not start naming all your variables single letters.
