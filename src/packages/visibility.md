# Visibility

By default, a class can only see the other classes 
in its package.

```java,no_run
package dungeon;

class BugBear {

}
```

```java,no_run
package village;

class Villager {

}
```

```java,no_run
package dungeon;

class Dwarf {
    BugBear fight() {
        // Can "see" BugBear and thus call its constructor,
        // access visible fields and methods, etc.
        return new BugBear();
    }

    // Cannot see Villager because it is in a different package.
}
```