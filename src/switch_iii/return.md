# return

If you explicitly `return` from inside a C-style switch then there is no need to have a `break`
to avoid fallthrough.

```java
class Main {
    void sayWhoTheyFought(String name) {
        switch (name) {
            case "Launch":
                IO.println("Fought Red Ribbon Army");
                IO.println("Fought 3 nameless convicts");
                return; // This will return from the whole method
            case "Goku":
                IO.println("Fought Pilaf");
                IO.println("Fought The Red Ribbon Army");
            case "Gohan":
                IO.println("Fought Frieza");
                IO.println("Fought Cell");
                IO.println("Fought Majin Buu");
        }
    }

    void main() {
        sayWhoTheyFought("Launch");
    }
}
```

This should be intuitive.
