# Defaults

You can give a default value for an element by writing `default` followed by a value.

You don't need to explicitly specify a value for any elements that have a default.

```java
enum Priority {
    HIGH,
    LOW
}

@interface Todo {
    String description();
    Priority priority() default Priority.LOW;
}

// Priority does not need to be specified since
// it has a default specified
@Todo(description="Write the code")
class Code {
    // But you can still specify it in situations where you want to
    @Todo(description="Write main method", priority=Priority.HIGH)
    void main() {
    }
}
```

If all values have defaults then you don't need to specify anything.

```java
enum Priority {
    HIGH,
    LOW
}

@interface Todo {
    String description() default "Do Stuff";
    Priority priority() default Priority.LOW;
}

@Todo
class Code {
}
```

And if the only element that doesn't have a default value is named `value`, and thats the only one you want to specify, you don't need to give its name.

```java
enum Priority {
    HIGH,
    LOW
}

@interface Todo {
    String value();
    Priority priority() default Priority.LOW;
}

@Todo("Really need to write something in here")
class Code {
}
```