# return

If you explicitly `return` from inside a C-style switch then there is no need to have a `break`
to avoid fallthrough.

```java
class Main {
    void sayWhoTheyFought(String name) {
        switch (name) {
            case "Launch":
                System.out.println("Fought Red Ribbon Army");
                System.out.println("Fought 3 nameless convicts");
                return; // This will return from the whole method
            case "Goku":
                System.out.println("Fought Pilaf");
                System.out.println("Fought The Red Ribbon Army");
            case "Gohan":
                System.out.println("Fought Frieza");
                System.out.println("Fought Cell");
                System.out.println("Fought Majin Buu");
        }
    }

    void main() {
        sayWhoTheyFought("Launch");
    }
}
```

This should be intuitive.
