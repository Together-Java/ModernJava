# Continue

Unless there is a `break`, while loops will usually run all the code in their body from top to bottom.

The only other situation this will not happen is if a `continue` statement is reached.

```java
~void main() {
// Will output a message for every number except 4
int x = 5;
while (x > 0) {
    if (x == 4) {
        continue;
    }
    System.out.println(x + " is a good number");
    x--;
}
~}
```

If a `continue` is reached the code in the loop stops running immediately but, unlike `break`,
the condition of the loop _is_ checked again. If it still evaluates to `true` then the code
in the loop will run again.
