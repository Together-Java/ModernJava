# Module Imports

A special kind of import is the "module import."

Just like a `*` at the end of a regular import will
import all the classes in that package, an `import module`
declaration will import all the classes in all the packages
contained within that module.

```java
// Same as writing
//
// import java.util.*;
// import java.lang.annotation.*;
// import java.lang.reflect.*;
// ... and so on for every package in the java.base module
import module java.base;

class Main {
    void main() {
        // You can now freely use any of the classes from the imported module
        Collection<String> c = List.of("do", "re", "mi");

        IO.println(c);
    }
}
```