# java.base

The `java.base` module is where all packages like `java.lang`, `java.util`, etc.
are defined. 

This means it contains classes used by nearly every Java program like `java.lang.String`,
`java.lang.Integer`, and `java.util.ArrayList`.

Because of this, it is the only module you do not need to explicitly require in a `module-info.java` file.

```java
module cool.code {
    // You can leave this line off
    // and it will still require java.base
    requires java.base;
}
```

And when you have a file that makes use of "The Anonymous Main class,"
Java will also act as if you had a module import for `java.base`. This
means that you don't actually need an explicit import for classes like `ArrayList`.

So if a file has the following

```java
void main() {
    var names = new ArrayList<String>();
    names.add("Him");
    names.add("Jim");
    names.add("Bim");
    IO.println(names);
}
```

It is equivalent to 

```java
import module java.base; 

class Main {
    void main() {
        var names = new ArrayList<String>();
        names.add("Him");
        names.add("Jim");
        names.add("Bim");
        IO.println(names);
    }
}
```

