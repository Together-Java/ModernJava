# Boxed Primitives

The fact that `int`, `double`, `char`, and `boolean` cannot have `null` values
can be limiting.

For this reason there are versions of those primitive[^primitive] types which do not have this restriction.

```java
void sayAge(Integer age) {
    if (age == null) {
        IO.println("Age is not yet known");
    }
    else {
        IO.println("Age is " + age);
    }
}

void main() {
    Integer age = null;
    sayAge(age);

    age = 26;
    sayAge(age);
}
```

We call these primitives which might be null "Boxed Primitives" because they are made by taking
the underlying thing and putting it in a "box."[^boxing]


[^primitive]: We call them "primitive" types because there isn't a way for you to implement them yourself in Java. They have to be given to you as a fundamental and magic sort of thing.

[^boxing]: Don't worry too much about the word box in this context. This will make more sense once you learn how to define your own types. I just wanted to at least try to gesture at why it has the silly name that it does.