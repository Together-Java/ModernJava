# Unreachable Code

If you write some code directly after a `break` or `continue`
that code will be "unreachable."

Java knows this and so won't let any code like that run.

```java
// This will not work
while (true) {
    continue;

    System.out.println("this is unreachable");
}
```