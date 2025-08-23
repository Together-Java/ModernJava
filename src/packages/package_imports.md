# Package Imports

If you want to import all of the classes in a package
all at once you can use a "package import."

To do this write `import` followed by the name of the
package and `.*`.

```java,no_run
package village;

public class Villager {}
```

```java,no_run
package village;

public class Dog {}
```

```java,no_run
package dungeon;

// Imports Village, Dog, and any other classes
// in the "village" package.
import village.*;

class Dwarf {
    Villager meet() {
        return new Villager();
    }

    Dog pet() {
        return new Dog();
    }
}
```

This has the upside of being only one line of code. This also has the
downside of being only one line of code - it is harder to figure out
from what package any particular class might be coming from.