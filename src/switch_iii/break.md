# break

After each case label in a C-style switch, you should write `break;`.[^cookout]

```java
class Main {
    void main() {
        String name = "Piccolo";
        switch (name) {
            case "Squidward":
                IO.println("Invited, but not coming.");
                break;

            case "Piccolo":
                IO.println("Coming to the cookout.");
                break;

            case "Spider-Man":
                IO.println("Not coming");
                break;
        }
    }
}
```

This is different from breaking out of a loop and won't break out of any surrounding loops.

```java
class Main {
    void main() {
        for (int i = 0; i < 3; i++) {
            // Will still run 3 times
            String name = "Piccolo";
            switch (name) {
                case "Squidward":
                    IO.println("Invited, but not coming.");
                    break;

                case "Piccolo":
                    IO.println("Coming to the cookout.");
                    break;

                case "Spider-Man":
                    IO.println("Not coming");
                    break;
            }
        }
    }
}
```

To break out of surrounding loops you can use a labeled break.

```java
class Main {
    void main() {
        outerLoop:
        for (int i = 0; i < 3; i++) {
            String name = "Piccolo";
            switch (name) {
                case "Squidward":
                    IO.println("Invited, but not coming.");
                    break;

                case "Piccolo":
                    IO.println("Coming to the cookout.");
                    break outerLoop; // Will break out of the loop

                case "Spider-Man":
                    IO.println("Not coming");
                    break;
            }
        }
    }
}
```

[^cookout]: [Who should be invited to the cookout?](https://www.youtube.com/watch?v=64SoFWJHSd8)