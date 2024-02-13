# Endless Loops

If a while loop will never end, we call that an endless loop.

This can happen if the condition is a constant like `while (true)`

```java,no_run
~void main() {
while (true) {
    System.out.println("This is the song that never ends");
}
~}
```

Or if the variables tested in the condition are not updated inside of the loop.

```java,no_run
~void main() {
// x is never changed
int x = 0;
while (x != 1) {
    System.out.println("It goes on and on my friends");
}
~}
```

Many games should never really "finish" so at the very start of that sort of program it is not uncommon
to see a `while (true)`.
