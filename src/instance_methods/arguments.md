# Arguments

Instance methods can take arguments the same as the methods you have
seen so far.

```java
class Muppet {
    String name;

    void singLyric(int verse) {
        if (verse == 1) {
            IO.println("Why are there so many");
        }
        else if (verse == 2) {
            IO.println("Songs about rainbows");
        }
        else {
            IO.println("And what's on the other side?");
        }
    }
}
```