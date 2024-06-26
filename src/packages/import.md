# Import

If you don't want to write out the fully qualified class name everywhere, and few do,
then you can use an `import`.

To import a class you write `import` followed by the fully qualified class name.
This makes it so that the "simple" class name will be usable.

```java,no_run
package village;

public class Villager {}
```

```java,no_run
package dungeon;

// For the rest of the file, you can
// just write "Villager" and Java will know
// what you mean.
import village.Villager;

class Dwarf {
    Villager meet() {
        return new Villager();
    }
}
```