# Counting Down

If you want to do the opposite, starting from a number like `100` and count down to `1`, 
the pattern will be similar.

You still have some variable tracking the current
number, but with a loop whose condition is that the number is greater than the number you want
to stop at, and a line at the bottom of the loop which decrements the current number.

```java
int currentNumber = 100;
while (currentNumber >= 1) {
    System.out.println(currentNumber);
    currentNumber--;
}
```

Similar to when counting up if the condition was not `currentNumber >= 1` and instead was
`currentNumber > 1`, the loop would stop at `2`

```java
int currentNumber = 100;
// Stops at 2
while (currentNumber > 1) {
    System.out.println(currentNumber);
    currentNumber--;
}
```