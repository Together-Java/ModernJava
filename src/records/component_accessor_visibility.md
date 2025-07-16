# Component Accessor Visibility

The accessor methods of a record are always public, so all the packages
that can see the class can access its components.

```java,no_run
package dungeon;

public record Dragon(double wingspan) {}
```

```java,no_run
import dungeon.Dragon;

void main() {
    var dragon = new Dragon(224.5);
    IO.println(
        // Method is visible.
        dragon.wingspan()
    );
}
```