# Package-Private Fields

Fields that are marked neither `public` nor `private` are "package-private."

```java
package village;

public class Well {
    // Neither of these can be used outside of the "village" package
    static final int NUMBER_OF_DEMONS = 4;
    boolean exorcismPerformed;
}
```