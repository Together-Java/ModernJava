# The Default Constructor

If a class is `public` and has a default constructor - i.e. the constructor you
get when you don't specify one - then the default constructor you get will be
`public`.

```java,no_run
package dungeon;

public class Skeleton {
    // No constructor specified
}
```

```java,no_run
package village;

import dungeon.Skeleton;

class Main {
    void main() {
        // We can say `new Skeleton()` here
        var skeleton = new Skeleton();
    }
}
```

If you write out a constructor yourself this will not be the case.

```java,no_run
package dungeon;

public class Skeleton {
    public final int bones;

    Skeleton() {
        this.bones = 206;
    }
}
```

```java,no_run
package village;

import dungeon.Skeleton;

class Main {
    void main() {
        // Now "new Skeleton()" will not work.
        var skeleton = new Skeleton();
    }
}
```