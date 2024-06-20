# Fully Qualified Class Name

In order to use a public class from a different package you can
write out the "fully qualified class name."[^fqcn]

This is the name of the class prefixed with the package it is in.

```java,no_run
package village;

public class Villager {}
```

```java,no_run
package dungeon;

class Dwarf {
    // Works because we write out the full name
    // and because Villager is public.
    village.Villager meet() {
        return new village.Villager();
    }
}
```

This hints that the "real name" of a class isn't what you write after `class`, but instead both that and the package name glued together.

[^fqcn]: People also often call this the "FQCN". Its a fun acronym to write, but I
have no clue how to say it out loud. "Faquacün?"