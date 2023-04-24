# Break

`break` works the same with `for` loops as it does with `while` loops.
Any time you hit a line with `break` you will immediately exit the loop.

```java
for (int i = 0; i < 1000; i++) {
    if (i == 5) {
        break;
    }
    System.out.println(i);
}
System.out.println("Over");

// 0
// 1
// 2
// 3
// 4
// Over
```