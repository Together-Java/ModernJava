# Methods

All the code you have seen up until this point has lived inside of `void main() {}`.

```java
void main() {
    IO.println("CODE GO HERE");
}
```

This isn't sustainable for a few reasons. One is that code can get big. Putting a thousand lines inside of one place can be a lot, let
alone the hundreds of thousands you need to be Minecraft or the millions you need to be Google.

Another is that there is almost always code that you will want to run at multiple places in a program.
Copy pasting that code can get old.

This is what methods are for. Methods let you split up your code into smaller, reusable chunks.[^def]

[^def]: The word method comes from a "method of getting things done." You might also hear methods referred to as "functions".
