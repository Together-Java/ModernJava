# Package-Private Constructors

A constructor without any other modifier is "package-private" in the
same way as methods and fields.[^private]

```java
package dungeon;

public class Slime {
    final int size;

    // This constructor is public, 
    // code in other packages can use it.
    public Slime() {
        this.size = 5;
    }

    // This constructor is package-private,
    // code in other packages cannot use it.
    Slime(int size) {
        this.size = size;
    }
}
```

[^private]: Your spider-sense might be tingling wondering if `private` constructors
are a thing. They are! I'll talk about them more in-depth later, but they can be
surprisingly useful.