# Public Methods

Even though a class might itself be marked `public`, the methods
within it will not be unless they are also `public`.

```java,no_run
package village;

// Now other packages will be able to see it
public class Villager {
    public void isVisible() {
        System.out.println("This method is callable from another package.");
    }

    void isNotVisible() {
        System.out.println("This method is not.")
    }
}
```

This applies also to static methods.

```java,no_run
package village;

public class Well {
    public static int drawWater() {
        System.out.println("""
            You need this to be both public and static to
            be able to write Well.drawWater()
            """);
        return 235;
    }
}
```
