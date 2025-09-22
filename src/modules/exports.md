# Exports

Inside your `module-info.java` file you declare which packages are
"exported" from that module.

```java,no_run
module reality {
    exports earth;
    exports sea;
    exports sky;
}
```

Any packages that do not have an `exports` declaration are "unexported packages."

The classes in unexported packages will not be visible to other modules
even if those classes are `public`.

```java,no_run
// Because the "backrooms" package is not exported
// from the "reality" module, other modules cannot
// observe classes within it.
package backrooms;

public class YellowCarpet {
}
```

```java,no_run
package sky;


// But classes within other packages of
// the "reality" module can see it just fine.
public class Cloud {
    private final YellowCarpet fabricOfExistence
        = new YellowCarpet();

    // ...
}
```