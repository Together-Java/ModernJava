# Challenges


Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Declare your own `@Favorite` and `@LeastFavorite`
annotations.

Use them to mark the code you have written so far that is your
favorite and the code that is your least favorite.

## Challenge 2.

Declare a `@LoFi` annotation. It should have an element for the `author`
and another element for the `song` that you were listening to on
the "[24/7 Lofi Hip Hop Radio - Beats to Relax/Study To](https://www.youtube.com/watch?v=jfKfPfyJRdk)"
stream when you were writing the annotated code.

Chill out to some tunes, write some code, and use that annotation.

## Challenge 3.

Write a method that takes in an `Object`. Use reflection to print out the values in that `Object`'s
declared fields. Skip any that are non-public but also any marked with a `@Skip` annotation
that you should also define.

```java
// CODE HERE

class Table {
    public boolean flowerPot = true;
    public String scissors = "green";

    @Skip
    public String cat = "tabby";
}

class Main {
    void main() {
        // CODE HERE
    }
}
```
