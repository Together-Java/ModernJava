# Comparison to Loops

Everything that can be accomplished by using loops can be accomplished
using recursion. This means it is always possible to take some
code using loops and translate it mechanically to code using
recursion.

```java
void seasonFoodRecursive(int times) {
    if (times == 0) {
        return;
    }
    else {
        IO.println("seasoning");
        seasonFoodRecursive(times - 1);
    }
}

void seasonFoodIterative(int times) {
    for (int i = 0; i < times; i++) {
        IO.println("seasoning");
    }
}
~
~void main() {
~    IO.println("Recursive");
~    seasonFoodRecursive(2);
~    IO.println("Iterative");
~    seasonFoodRecursive(2);
~}
```

Not everything that can be accomplished by using recursion can be accomplished
using loops. At least without introducing some data structure to track what would
otherwise be stored in Java's call stack. The following video goes a little further in depth
as to why.

<iframe width="560" height="315" src="https://www.youtube.com/embed/i7sm9dzFtEI?si=en1phfHlOSCkoV6r" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


This is part of why its important to power through recursion. There are things
that can only be solved with it and there are things that are more easily solved with it.