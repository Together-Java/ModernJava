# Comparison to Delegation

A related technique to recursion is "delegation."

This is when you have one method call a different arity
version of itself.

```java
// This method is delegated to
void seasonFood(int shakes) {
    for (int i = 0; i < shakes; i++) {
        IO.println("1 shake of pepper");
    }
}

// by this method, which provides a "default" value of 2
void seasonFood() {
    seasonFood(2);
}

void main() {
    seasonFood();
}
```

This is distinct from recursion since, while the method delegated to
might have the same name as the one delegating, different
overloads of methods are considered distinct methods.

`void seasonFood()` is therefore a different method than `void seasonFood(int)`.