# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Make your own class named `OneToTen` which implements `Iterable<Integer>`
and will yield the numbers from `1` to `10`.

This will require making a class which implements `Iterator<Integer>` as well.

```java,editable
// CODE HERE

class OneToTen implements Iterable<Integer> {
    // CODE HERE
}

class Main {
    void main() {
        var oneToTen = new OneToTen();

        // Should output
        // 1 2 3 4 5 6 7 8 9 10 
        // twice
        for (int i : oneToTen) {
            IO.print(i);
            IO.print(" ")
        }
        IO.println();

        // If it only happens once, you might be
        // mistaken about the difference between
        // Iterable and Iterator
        for (int i : oneToTen) {
            IO.print(i);
            IO.print(" ")
        }
        IO.println();
    }
}
```

## Challenge 2.

Make a class named `StringIterable` which implements `Iterable<String>`.

Its constructor should take a `String` and it should let you iterate over
each character.

```java,editable
// CODE HERE

class Main {
    void main() {
        var stringIterable = new StringIterable("abc");
        
        // Should output
        //
        // a
        // b
        // c
        // -------
        // a
        // b
        // c
        for (char c : stringIterable) {
            IO.println(c);
        }
        IO.println("-------");
        for (char c : stringIterable) {
            IO.println(c);
        }
    }
}
```

## Challenge 3.

The following code will crash with a `ConcurrentModificationException`.
Rewrite it so that it does not.

```java,editable
import java.util.ArrayList;

class Main {
    void main() {
        var trash = new ArrayList<String>();
        trash.add("gloves");
        trash.add("staff");
        trash.add("glasses");

        for (var item : trash) {
            if (item.equals("glasses")) {
                trash.remove(item);
            }
        }
    }
}
```