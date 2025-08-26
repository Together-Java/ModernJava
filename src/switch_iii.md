# Switch III


<img src="/switch_iii/header.png" height="200px"/>

The switch statement in Java originally came from a little language you might know
about called `C`.

In `C` switches work slightly differently than the ones you have seen so far in Java.
But, due to this history, there is another kind of switch that doesn't use arrows (`->`)
and instead uses a colon (`:`).

```java
class Main {
    boolean shouldBeMainCharacter(String name) {
        switch (name) {
            case "Gohan":
                return true;
            case "Goku":
            default:
                return false;
        }
    }

    void main() {
        IO.println(
            shouldBeMainCharacter("Goku")
        );
    }
}
```

This "C-Style Switch" is important to learn chiefly because, for a long time,
it was the only switch in Java. Therefore in your coding life you are very likely to
run into it.