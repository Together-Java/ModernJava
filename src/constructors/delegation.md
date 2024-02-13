# Delegation

It is common for overloaded constructors to be "shortcuts" for eachother.

That is, if one overload takes two arguments another will take just one argument
and do the same logic as the first but fill in a default value for the un-provided value.

```java,no_run
class Muppet {
    final String name;
    final boolean talented;

    Muppet(String name) {
        this.name = name;
        this.talented = true;
    }

    Muppet(String name, boolean talented) {
        this.name = name;
        this.talented = talented;
    }
}
```

A downside of this is that any validation logic done in one constructor needs to be copy pasted to
the other.

```java,no_run
class Muppet {
    final String name;
    final boolean talented;

    Muppet(String name) {
        if (name.length() == 0) {
            throw new RuntimeException("Cannot have blank name");
        }
        this.name = name;
        this.talented = true;
    }

    Muppet(String name, boolean talented) {
        if (name.length() == 0) {
            throw new RuntimeException("Cannot have blank name");
        }
        this.name = name;
        this.talented = talented;
    }
}
```

To avoid this situation, you can have one constructor "delegate" to another.

To do this you write `this` in one constructor and call it as if it were a method.
This will run the logic of the constructor which matches the values passed in.

```java,no_run
class Muppet {
    final String name;
    final boolean talented;

    Muppet(String name) {
        // Will use the other constructor, but with false filled in
        // as a default value
        this(name, false);
    }

    Muppet(String name, boolean talented) {
        // This logic now only needs to live in one place.
        if (name.length() == 0) {
            throw new RuntimeException("Cannot have blank name");
        }
        this.name = name;
        this.talented = talented;
    }
}
```