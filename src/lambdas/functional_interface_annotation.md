# @FunctionalInterface

If an interface is marked with the `@FunctionalInterface` annotation,
Java will verify that it fulfils the requirements for a functional interface.

```java
@FunctionalInterface
interface BankRunner {
    void runOnBank();
}
~void main() {}
```

This is similar to the `@Override` annotation in that it doesn't affect how code works
but just adds in an extra guard rail.

```java,does_not_compile
@FunctionalInterface
interface BankRunner {
    // More than one required method, will error
    void runOnBank();
    int applyInflation(int money);
}
~void main() {}
```