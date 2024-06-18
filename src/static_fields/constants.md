# Constants

Because static fields are global to the entire program, they are the
preferred mechanism for storing "constants."

Constants are things that you don't expect to change, so you would also
mark such fields as `final`.

```java
class MathConstants {
    static final double PI = 3.14;
}

// Then in other parts of your code you can reference MathConstants.PI
```


