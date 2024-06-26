# Global Fields

Global fields, accordingly, were always a lie.

```java
int number = 0;

void main() {
    System.out.println(number);
    number++;
    System.out.println(number);
}
```

They are just normal fields in the anonymous main class.

```java
class Main {
    int number = 0;

    void main() {
        System.out.println(number);
        number++;
        System.out.println(number);
    }
}
```

This means that once you move to programs in multiple files they are no longer global
to your program - just the code in the main class.[^bummer]

[^bummer]: Huge bummer, but we will learn how to make actually global things later.