# The Canonical Constructor

A record is always given a constructor which matches
its list of record components.

```java,no_run
record Person(String name, int age) {}

void main() {
    // This call to new Person(...) matches up with 
    // the record declaration.
    var person = new Person("Ancient Dragon Man", 2000);
}
```

Similar to the "default constructor" given to regular classes, this
is what you get for "free" with the declaration of a record.