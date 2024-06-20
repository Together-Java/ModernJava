# Package-Private Methods

If a method is neither `public` or `private` then it can
be used only by code in the same package.

We call these methods "package-private" because they are
"private" to code outside the package.

```java
package village;

public class Villager {
    void isNotVisible() {
        System.out.println("""
            This method can be called from code in the "village"
            package, but not from other packages.
            """);
    }
}
```

Which again applies to static methods as well.
