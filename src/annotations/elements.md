# Elements

Annotation interfaces can contain any number of elements.

```java,no_run
@interface Todo {
    String description();
}
```

These are declared in the same way as methods in an interface, save for some
important restrictions.

The method should take no arguments.

```java,no_run,does_not_compile
@interface Todo {
    // Cannot take arguments
    String description(int x);
}
```

And the return value needs to be one of a few built-in types like `Class`, `String`, `int`, `boolean`, etc.[^fulllist], an `enum`, or an array of one of those.

```java,no_run,does_not_compile
enum Priority {
    HIGH,
    LOW
}

class PersonInCharge {}

@interface Todo {
    // String ✅
    String description();

    // int ✅
    int someNumber();

    // boolean ✅
    boolean isImportant();

    // Class ✅
    Class<?> someRelatedClass();

    // Arrays ✅
    String[] notes();

    // Enums ✅
    Priority priority();

    // Other Classes ❌
    PersonInCharge personInCharge();
}
```

[^fulllist]: You can find the full list [here](https://docs.oracle.com/javase/specs/jls/se23/html/jls-9.html#jls-9.6). It is a short list.
