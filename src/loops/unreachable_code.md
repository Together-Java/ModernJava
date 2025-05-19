# Unreachable Code

If you write some code directly after a `break` or `continue`
that code will be "unreachable."

Java knows this and so won't let any code like that run.

```java,does_not_compile
~void main() {
// This will not work
while (true) {
    continue;

    IO.println("this is unreachable");
}
~}
```
