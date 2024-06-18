# Scope

In the definition of a static method you can use variables like normal
and you can reference other static fields and methods.

```java,no_run
class ScopeExample {
    static final int CAN_ACCESS = 3.14;

    static void canCall() {
    }

    static void doStuff() {
        canCall();
        System.out.println(ScopeExample.CAN_ACCESS);
    }
}
```

But you cannot access any non-static methods or fields. They are not in scope.

```java,no_run,does_not_compile
class ScopeExample2 {
    final int CANNOT_ACCESS = 3.14;

    void cannotCall() {
    }

    static void doStuff() {
        cannotCall();
        System.out.println(
            CANNOT_ACCESS
        );
    }
}
```
