# Initialization

By default, static fields will be given the same default initial value as other fields.

So a static `int` field will be initialized to zero, a static `String` field
will be initialized to `null`, etc.

```java
class Main {
    static int count;
    static String name;

    void main() {
        System.out.println(count); // 0
        System.out.println(name); // null
    }
}
```

If you want to initialize them to a different value you do not do that in a constructor
like you would a normal field. 

You can give them a value directly with `=`.

```java
class Main {
    static int count = 5;
    static String name = "bob";

    void main() {
        System.out.println(count); // 5
        System.out.println(name); // bob
    }
}
```

Or you can initialize them in a "static block". This looks like the word `static`
followed by some braces `{}` with code in the middle.[^confusing]

```java
class Main {
    static int count;
    static String name;

    static {
        count = 5;
        name = "bob";
    }

    void main() {
        System.out.println(count); // 5
        System.out.println(name); // bob
    }
}
```

[^confusing]: The rules for static blocks are actually crazy complicated. Try not to do anything "interesting" in them.