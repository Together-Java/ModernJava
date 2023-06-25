# Labeled Continue

Labeled continues also work the same in `for` loops as `while` loops, but with the hopefully expected caveat that
the statement of a `for` loop will always run when you get to the top of it.[^uncommon]

```java
label:
for (int i = 0; i < 4; i++) {
    for (int j = 0; j < 3; j++) { 
        System.out.println ("" + i + ", " + j);
        if (i == 2) {
            // i++ will run
            continue label;
        }   
    }
}
// 0, 0
// 0, 1
// 0, 2
// 1, 0
// 1, 1
// 1, 2
// 2, 0
// 3, 0
// 3, 1
// 3, 2
```