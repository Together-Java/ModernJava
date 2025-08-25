# Streams

Programs often have to transform all of the elements in a collection
in order to produce a new collection.

For instance: take all the people in a `List`, remove any who are
older than 65, and extract their names into a set.

```java
import module java.base;

record Person(String name, int age) {}

class Main {
    void main() {
        List<Person> people = List.of(
            new Person("Jess", 29),
            new Person("Sally", 72),
            new Person("Bess", 41)
        );

        Set<String> names = new HashSet<>();
        for (var person : people) {
            if (person.age() < 65) {
                names.add(person.name());
            }
        }

        IO.println(names);
    }
}
```

While such transformations can always be done in "normal code,"
it can be preferable to use "streams."

```java
import module java.base;

record Person(String name, int age) {}

class Main {
    void main() {
        List<Person> people = List.of(
            new Person("Jess", 29),
            new Person("Sally", 72),
            new Person("Bess", 41)
        );

        Set<String> names = people.stream()
            .filter(person -> person.age() < 65)
            .map(Person::name)
            .collect(Collectors.toSet());

        IO.println(names);
    }
}
```