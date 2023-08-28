# Continue

`continue` works slightly differently with `for` loops than how it does with `while` loops.

Any time you hit a line with `continue` you will immediately jump back to the top of the loop, but
unlike with a `while` loop, the statement which updates your variable will still run.

```java
for (int i = 0; i < 5; i++) {
    if (i == 2) {
        // i++ will still run
        continue;
    }
    System.out.println(i);
}

// 0
// 1
// 3
// 4
```

So the above `for` loop is not equivalent to this `while` loop.

```java
int i = 0;
while (i < 5) {
    if (i == 2) {
        continue;
    }
    System.out.println(i);

    i++;
}

// 0
// 1
// ... spins forever ...
```

It is equivalent to this one.

```java
int i = 0;
while (i < 5) {
    if (i == 2) {
        i++
        continue;
    }
    System.out.println(i);

    i++;
}

// 0
// 1
// 3
// 4
```
