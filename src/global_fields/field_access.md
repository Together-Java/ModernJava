# Field Access


You can access global fields by writing their name. This works from within
top level methods as well as instance methods of classes.[^different]

```java
final String monster = "Dracula";

class Mash {
    void itWasThe() {
        System.out.println(monster + " and his son");
    }
}

void main() {
    System.out.println(monster + " was there");

    Mash mash = new Mash();
    mash.itWasThe();
}
```

[^different]: This is so convenient it is actually going to be a bummer once you learn what is going on here
and can't do it for most of your programs anymore.