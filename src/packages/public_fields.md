# Public Fields

Similarly to methods, for a field to be used from a different package
it must be marked `public`.

```java
package village;

public class Well {
    // Both of these you can use from a different package
    public static final int DEPTH = 10;
    public int remainingWater;
}
```
