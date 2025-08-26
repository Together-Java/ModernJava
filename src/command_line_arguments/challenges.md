# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Make a program under `src/CLI.java`. The rest of these challenges will all be adding
features to that program.

```java
class CLI {
    // CODE HERE

    void main(String[] args) {
        // CODE HERE
    }
}
```

First, make it so that `java src/CLI.java` prints "No arguments provided"
and immediately exits.

## Challenge 2.

Make it so that `java src/CLI.java 8` will print `64` and then exit.
If you ran `java src/CLI.java 5` it would print `25` and so on.
For any number it should print it's square.

## Challenge 3.

Make the operation to perform overridable. `java src/CLI.java --operation square 8`
should do the same thing as `java src/CLI.java 8`. `java src/CLI.java --operation factorial 8`
should print out `8` factorial (which is `40320`) instead of `64`.

## Challenge 4.

If a `-d` argument is provided then, instead of printing the result, the program
should write the result to a file at the specified path.

So `java src/CLI.java -d out.txt 9` should write `81` into a file named `out.txt`.
The order that `-d` and `--operation` are provided should not matter. `java src/CLI.java -d out.txt --operation factorial 3` and `java src/CLI.java --operation factorial -d out.txt 3` should behave exactly the same.

## Challenge 5.

Make `java src/CLI.java --help` print out a help message describing the different flags
you can provide and their meanings. To see what this should look somewhat like
first run `java --help`.