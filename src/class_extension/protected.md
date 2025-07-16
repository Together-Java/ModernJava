# Protected

If you want code to be accessible by a subclass defined in another package
but not be fully `public`, that is where the `protected` modifier is useful.

`protected` fields, methods, and constructors have the same visibility as package-private ones.
This means classes in the same package can see them but classes in other packages cannot.
The only addition is that it is visible to extending classes regardless of package.

```java
package oceanography;

class BodyOfWater {
    // Both the depth field and the following
    // constructor are only visible to subclasses
    // and classes in the "oceanography" package.
    protected long depth;

    protected BodyOfWater(long depth) {
        if (this.depth < 0) {
            throw new IllegalArgumentException();
        }
        this.depth = depth;
    }
}
```

```java
package bigwater;

class Ocean extends BodyOfWater {
    String name;

    Ocean(String name, long depth) {
        this.name = name;
        // The super(depth) constructor is only usable because it is
        // visible.
        super(depth);
    }
}
```

This is useful for providing methods that you really only expect to be useful for
producing subclasses but that you don't want to be available to everyone.