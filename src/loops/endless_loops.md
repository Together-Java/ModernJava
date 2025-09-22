# Endless Loops

If a while loop will never end, we call that an endless loop[^hot].

This can happen if the condition is a constant like `while (true)`

```java,no_run
~void main() {
while (true) {
    IO.println("This is the song that never ends");
}
~}
```

Or if the variables tested in the condition are not updated inside of the loop.

```java,no_run
~void main() {
// x is never changed
int x = 0;
while (x != 1) {
    IO.println("It goes on and on my friends");
}
~}
```

Many games should never really "finish" so at the very start of that sort of program it is not uncommon
to see a `while (true)`.

[^hot]: If you run an endless loop that does nothing but loop your computer might start overheating. This is a natural part of the process and ultimately healthy for your CPU fans.
