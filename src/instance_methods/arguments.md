# Arguments

Instance methods can take arguments the same as the methods you have
seen so far.

```java
class Muppet {
    String name;

    void singLyric(int verse) {
        if (verse == 1) {
            System.out.println("Why are there so many");
        }
        else if (verse == 2) {
            System.out.println("Songs about rainbows");
        }
        else {
            System.out.println("And what's on the other side?");
        }
    }
}
```