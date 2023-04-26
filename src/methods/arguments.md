# Arguments

As part of a method declaration, you can include a comma separated list of "arguments"
to that method.

These arguments let you change what happens when a method runs.

```java
int square(int x) {
    return x * x;
}

void main() {
    // 9
    System.out.println(square(3));
}
```