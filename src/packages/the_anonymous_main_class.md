# The Anonymous Main Class

You are only allowed to make an anonymous main class
inside the default package.

```java,no_run
// Allowed
void main() {
    System.out.println("Hello, world");
}
```

```java,does_not_compile
// Not Allowed
package myprogram;

void main() {
    System.out.println("Hello, world");
}
```

This means that for classes in packages you have to wrap them in 
an explicitly named class like everything else.

```java,no_run
// Allowed
package myprogram;

class Main {
    void main() {
        System.out.println("Hello, world");
    }
}
```