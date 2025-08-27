# First Steps


<img src="/first_steps/header.png" height="200px"/>


If you made it through the [Getting Started section](./getting_started.md) you've successfully run this program.

```java
void main() {
    IO.println("Hello, World!");
}
```

This "prints" - not in the sense of a physical printer, but like "displays on the screen" -
the text `"Hello, World!"`.

Its a tradition for this to be your first program in any language.

We aren't quite at the point where I can explain what `void main()` means, but
all you need to know for now is that it is what Java looks for to know where to start the program.

```java,no_run
void main() {
    < WRITE YOUR CODE HERE >
}
```

So for all intents and purposes, this is the whole program.

```java
~void main() {
IO.println("Hello, World!");
~}
```

This bit of magic here - `IO.println` - is a "statement" that "prints" the text inside the `(` and `)` as well as a "new line" to the screen.

The "`IO`" part stands for "Input/Output" then it is **print** with new **l**i**n**e.

If you were to replace it with `IO.print`, then the output would lack that new line. This makes the following program be functionally identical to the first.

```java
~void main() {
IO.print("Hello, ");
IO.print("World");
IO.println("!");
~}
```

Which, when we add back `void main()`, looks like this.

```java
void main() {
    IO.print("Hello, ");
    IO.print("World");
    IO.println("!");
}
```

You should get in the habit of, whenever you see some bit of code, trying to physically type it out, run it,
tweak it, and play with it.

So try playing around with this program. If you actively engage then you will retain information better.
