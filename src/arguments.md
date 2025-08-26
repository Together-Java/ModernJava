# Arguments


<img src="/arguments/header.png" height="200px"/>

If methods always had to do the same thing each time they were run, they wouldn't be that useful.

The way to customize what happens when a method is called is to have them take "arguments."

```java
void sayHello(String name) {
    IO.println("Hello " + name + "!");
}

void main() {
    // Hello Joshua!
    sayHello("Joshua");
    // Hello Claire!
    sayHello("Claire");
}
```
