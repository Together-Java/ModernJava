# Accumulators

A common thing to do with loops is to "accumulate"
some value each time you go through the loop.

```java
class Main {
    int timesTwo(int x) {
        int total = 0;
        while (x > 0) {
            total += 2;
            x--;
        }

        return total;
    }

    void main() {
        IO.println(
            timesTwo(4)
        );
    }
}
```

To accomplish the same task with recursion you need two things.

The first is an extra "accumulator" argument to your function.
This is what you will update with the new value each time
you recurse.

The second is an overload of your method which takes all the
same arguments minus that accumulator. This overload should
immediately delegate to the one that takes all the arguments
with some starting value for the accumulator.

```java
class Main {
    int timesTwo(int x, int accumulator) {
        if (x > 0) {
            return timesTwo(x - 1, accumulator + 2);
        }
        else {
            return accumulator;
        }
    }

    int timesTwo(int x) {
        return timesTwo(x, 0);
    }

    void main() {
        IO.println(
            timesTwo(4)
        );
    }
}
```

The reason we need to do this is because, unlike with a loop, it is difficult to share variables
across recursive calls. Adding an extra function parameter lets us have a place
to put what would otherwise be a local variable updated by a loop.[^naming]

[^naming]: You may have noticed that the name changed from `total` to `accumulator`. There
is no particularly good reason for this other than to highlight that the total being built
up is an example of an "accumulator."