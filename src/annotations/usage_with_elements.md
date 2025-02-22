# Usage with Elements

If an annotation is declared with elements then you must specify
values for those elements when annotating a part of your program.

```java,no_run
@interface Todo {
    String description();
}

@Todo(description="Actually write code")
class Code {
}
```

For `String`, `int`, and `boolean` elements you do this using their corresponding literals.
For `Class` elements you use `ClassName.class`. And for arrays you use array initializers.

```java,no_run
enum Priority {
    HIGH,
    LOW
}

@interface Todo {
    String description();

    int someNumber();

    boolean isImportant();

    Class<?> someRelatedClass();

    String[] notes();

    Priority priority();
}

@Todo(
        description = "Write some code",
        someNumber = 444,
        isImportant = false,
        someRelatedClass = ArrayList.class,
        notes = {
                "this example is potentially confusing",
                "it isn't high priority enough to fix"
        },
        priority = Priority.LOW
)
class Code {

}
```

If the only element you need to provide is named `value`, then you don't need to give its name.


```java,no_run
@interface Todo {
    // The name "value" is special
    String value();
}

@Todo("Write some code")
class Code {
}
```
