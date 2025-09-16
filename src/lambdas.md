# Lambdas

<img src="/lambdas/header.png" height="200px"/>


Making an implementation of `interface`s that
only require one method turns out to be a common
task for a Java developer.

```java,no_run
interface Band {
    void playHitSong();
}

class Starcadian implements Band {
    @Override
    public void playHitSong() {
        IO.println("ultralove");
    }
}
```

As such there is a mechanism called "lambdas"
which lowers the effort required to do so.

```java
interface Band {
    void playHitSong();
}

class Main {
    void main() {
        Band starcadian = () -> IO.println("ultralove");
        starcadian.playHitSong();
    }
}
```
