# Value Based Identity

While reference based identity can be useful, its often not what you want for keys in a `HashMap`.
Ideally if you are looking up `"Tow Mater"` you shouldn't have to be careful to ensure its the *same*
instance of `String`, all you care about is that it contains the right characters.

We call this notion of identity "value based." Two things are the same if they contain the same data - i.e. if they represent the same value.

```java
class Main {
    void main() {
        // Strings A and B are distinct instances
        var stringA = new String(new char[] { 'a', 'b', 'c' });
        var stringB = new String(new char[] { 'a', 'b', 'c' });

        // but they will give the same hashCode
        IO.println(stringA.hashCode());
        IO.println(stringB.hashCode());

        // and will be equal to eachother
        IO.println(stringA.equals(stringB));
        IO.println(stringB.equals(stringA));
    }
}
```

`String`s, all the numeric types like `Integer` and `Double`, as well as `Boolean`s are defined
in this way.[^difference] So will any `record`s and `enum`s you make[^bydefault].

```java
~void main() {
~    new Main().main();    
~}
~
record Pos(int x, int y) {}

class Main {
    void main() {
        // Positions A and B are distinct instances but hold the same values
        var posA = new Pos(5, 5);
        var posB = new Pos(5, 5);

        // therefore they will give the same hashCode
        IO.println(posA.hashCode());
        IO.println(posB.hashCode());

        // and will be equal to eachother
        IO.println(posA.equals(posB));
        IO.println(posB.equals(posA));
    }
}
```


[^difference]: There is an important distinction here between things where `.equals` and `.hashCode` are simply defined in terms of value based equality and whether the objects themselves have identity. Operations like `==` operate on what we might call an "intrinsic identity." Problem for later.

[^bydefault]: At least by default.