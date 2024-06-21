# Component Accessors

For each record component, an accessor
method will be available that has the name of that component.

You use these to access the values of components.

```java,no_run
record Dog(String name) {}
```

```java
~record Dog(String name) {}
class Main {
    void main() {
        var dog = new Dog("Hunter");

        // .name() accessor is available
        String name = dog.name();

        System.out.println(name);
    }
}
```
