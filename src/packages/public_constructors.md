# Public Constructors

For a constructor you write to be usable across packages[^youguessed] it needs
to be marked `public`.

```java,no_run
package dungeon;

public class Skeleton {
    public final int bones;

    public Skeleton() {
        this.bones = 206;
    }
}
```

```java,no_run
package village;

import dungeon.Skeleton;

class Main {
    void main() {
        // Now this works
        var skeleton = new Skeleton();

        // And we get the right number of bones!
        System.out.println(skeleton.bones);
    }
}
```


[^youguessed]: You guessed it!