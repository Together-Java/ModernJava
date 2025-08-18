# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.


Make a `Library` class. It should have four exposed methods

- `add` which takes a `Book` and adds it to the library.
- `list` which returns an `ArrayList<String>` of all the `Book`s in the library.
The `String`s in this list should be the [ISBN](https://en.wikipedia.org/wiki/ISBN)
of the book.
- `find` which takes a `String` representing the ISBN and returns a full `Book` record.
- `remove` which takes a `String` representing the ISBN and removes that `Book` from the
library.

Use a `HashMap` for storing this info in the `Library`.

```java,editable
record Book(String isbn, String title, String author) {}

class Library {
    // CODE HERE
}

class Main {
    void main() {
        Library publicLibrary = new Library();
        publicLibrary.add(new Book("978-0-8041-3902-1", "The Martian", "Andy Weir"));
        publicLibrary.add(new Book("978-0062060624", "The Song of Achilles", "Madeline Miller"));

        IO.println(publicLibrary.list());

        Book b1 = publicLibrary.find("978-0062060624");
        IO.println(b1); // The Song of Achilles

        Book b2 = publicLibrary.find("123");
        IO.println(b2); // null

        publicLibrary.remove("978-0062060624");

        Book b3 = publicLibrary.find("978-0062060624");
        IO.println(b3); // null

        IO.println(publicLibrary.list());
    }
}
```

## Challenge 2.

Write a method which takes as an argument an `ArrayList<String>`
and returns a `HashMap<String, Integer>` where each key is
a `String` from the original `ArrayList` and each value is the number
of times it appeared in that `ArrayList`.

```java,editable
class Main {
    HashMap<String, Integer> count(ArrayList<String> words) {
        // CODE HERE
    }

    void main() {
        ArrayList<String> w = new ArrayList<>();
        w.add("duck");
        w.add("duck");
        w.add("duck");
        w.add("goose");
        w.add("duck");
        w.add("duck");
        w.add("duck");
        w.add("duck");
        w.add("duck");
        w.add("duck");
        w.add("duck");
        w.add("duck");
        w.add("goose");
        w.add("zebra");

        // {duck=11,goose=2,zebra=1}
        IO.println(
            count(w)
        );
    }
}
```

If you feel like this is hard to do with just `.put` and `.get`, you can 
check for [other methods on HashMap that can help you](https://docs.oracle.com/en/java/javase/24/docs/api/java.base/java/util/HashMap.html).

## Challenge 3.

Without calling any methods on the `HashMap`, make it so that `map.get(person)` returns `null`.

```java
class Person {
    int age;

    Person(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "Person[age=" + age + "]";
    }

    @Override
    public boolean equals(Object o) {
        if (o instanceof Person p) {
            return age == p.age;
        }
        else {
            return false;
        }
    }

    @Override
    public int hashCode() {
        return Objects.hash(age);
    }
}

class Main {
    void main() {
        var person = new Person("Patrocolus");
        var map = new HashMap<Person, String>();
        map.put(person, "Achilles");

        // -------------

        // CODE HERE
        // Do not directly touch "map"

        // -------------

        // Should output `null`
        IO.println(map.get(person));
    }
}
```