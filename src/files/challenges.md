# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Write a file named `hello.txt` and give it `Hello, world`
as contents.

## Challenge 2.

Write a program that asks the user for a number and writes it into
a file named `numbers.txt`. 

## Challenge 3.

Update the previous program so that the list of numbers entered by a user
is stored in the file. So if they give `1`, `2`, and `3` the file should contain
something like the following.

```
1
2
3
```

Hint: `\n` is how you embed a newline character in `String`. You might find it useful.

## Challenge 4.

Update the previous program to also display the biggest number given so far
if the user types `biggest` instead of a number.


## Challenge 5.

Make the previous program behave sensibly if the file contains data that is not numbers.

## Challenge 6.

Complete this program.

```java
import java.nio.file.Path;
import java.io.IOException;

class Main {
    record Person(String name, int age) {}

    void main() throws IOException {
        var people = new Person[] {
            new Person("Steve Smith", 15),
            new Person("Stan Smith", 42),
            new Person("Rodger", 1601)
        };

        var path = Path.of("people.txt");

        save(path, people);

        people = load(path);

        System.out.println(people[0]);
        System.out.println(people[1]);
        System.out.println(people[2]);

    }

    void save(Path path, Person[] people) throws IOException {
        // Save to a file
    }

    Person[] load(Path path) throws IOException {
        return null; // Make actually return an array
    }
}
```


