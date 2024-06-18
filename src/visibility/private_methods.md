# Private Methods

If a class has a method that it uses but that you do not want other code to see,
you can mark it `private`.

```java,no_run
class RiceCooker {
    int temperature;

    private boolean shouldTurnOff() {
        return temperature > 100;
    }

    void operate() {
        if (shouldTurnOff()) {
            turnOff();
        }
        else {
            // ...
        }
    }
}
```

This makes it so that code in `RiceCooker.java` can see and call the `shouldTurnOff` method but code in other files cannot.

This is useful if you want to box up some logic but don't want to have to think about
what happens if other code calls it.