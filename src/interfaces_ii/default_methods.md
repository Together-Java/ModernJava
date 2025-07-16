# Default Methods

Interfaces can specify a `default` implementation
for a method.

```java,no_run
interface Dog {
    void bark();

    default void barkLoudly() {
        IO.print("(loudly) ");
        bark();
    }
}
```

Classes which implement interfaces do not need an explicit implementation
for methods which have a default.[^all]

```java,no_run
interface Dog {
    void bark();

    default void barkLoudly() {
        IO.print("(loudly) ");
        bark();
    }
}

class Poodle implements Dog {
    @Override
    public void bark() {
        IO.println("bark!")
    }
}
```

If the default implementation is not what you want, then that implementation
can be overrided.

```java,no_run
interface Dog {
    void bark();

    default void barkLoudly() {
        IO.print("(loudly) ");
        bark();
    }
}

class Poodle implements Dog {
    @Override
    public void bark() {
        IO.println("bark!")
    }

    @Override
    public void barkLoudly() {
        IO.println("BARK!")
    }
}
```

If all of the methods on an interface have a default then you don't need to provide an implementation for any of them.[^allmethods]

```java
interface Cat {
    default void meow() {
        IO.println("meow");
    }
}

class Tabby implements Cat {
    // Nothing needed to implement Cat
}
```

[^allmethods]: This is rarely useful, but not never.