# @Override

Just like when defining your own `equals`, `hashCode`, and `toString` you
can use `@Override` when implementing methods that come from an interface.

```java
interface Dog {
    void bark();

    String fetch(String ball);
}

class Mutt implements Dog {
    @Override
    public void bark() {
        IO.println("Bark");
    }

    @Override
    public String fetch(String ball) {
        return ball + " (with drool)";
    }
}
```


Right now there isn't a mechanical use for this since Java will yell at you if 
you defined the interface method wrong anyways, but there will be later. A small benefit
is that it makes it easier to tell at a glance which methods come from an interface
and which do not.