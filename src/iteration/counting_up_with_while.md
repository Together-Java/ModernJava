# Counting Up with while

Say your loop is intended to run some code for every number from `1` to `100`.

The general pattern for code like this is to have some variable which tracks the current
number, a loop whose condition is that the number is less than the number you want
to stop at, and a line at the bottom of the loop which increments the current number.

```java
int currentNumber = 1;
while (currentNumber <= 100) {
    System.out.println(currentNumber);
    currentNumber++;
}
```

Take note that in this example the condition is `currentNumber <= 100`, so the code in the 
loop will run when `currentNumber` is equal to `100`. If the condition was `currentNumber < 100`
it would stop at `99`.

```java
int currentNumber = 1;
// Stops at 99
while (currentNumber < 100) {
    System.out.println(currentNumber);
    currentNumber++;
}
```