# Counting Down

One example of a recursive function is one that counts down.

You start by taking a number as an argument. If that number
is greater than 0 you "recurse" with a
number one lower than you were given. if it isn't you are done. 

```java
void countDown(int x) {
    if (x > 0) {
        System.out.println("DONE");
    }
    else {
        System.out.println("x: " + x);
        countDown(x - 1);
    }
}

void main() {
    countDown(5);
}
```

In this situation `x <= 0` is our base case since that is the situation where we don't
recurse. Each time we do recurse, we get closer to that base case. `x - 1` is always going
to be closer to x being less or equal to 0.

All of this is equivalent to a `while` loop that looks like the following.

```java
void countDown(int x) {
    while (x > 0) {
        System.out.println("x: " + x);
        x = x - 1;
    }
    System.out.println("DONE");
}

void main() {
    countDown(5);
}
```
