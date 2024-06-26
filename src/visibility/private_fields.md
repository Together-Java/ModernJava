# Private Fields

Similar to private methods, you can also mark a field as private.

```java
class Kaiju {
    private int timesLostToGodzilla;

    Kaiju() {
        this.timesLostToGodzilla = 0;
    }

    void fightGodzilla() {
        this.timesLostToGodzilla++;
    }

    boolean isLoser() {
        return this.timesLostToGodzilla > 0;
    }
}
```

This makes it so that code in other files cannot see or change the field directly.


