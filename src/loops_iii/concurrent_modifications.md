# Concurrent Modifications

If you are looping over a collection with a for-each loop you generally
cannot remove things from that collection at the same time. Doing so should
trigger a `ConcurrentModificationException`.[^should]

```java,panics
~import java.util.ArrayList;
~
record Sandwich(
    int turkeySlices,
    int cheeseSlices,
    boolean mayo
) {}

~class Main {
~   void main() {
ArrayList<Sandwich> sandwiches = new ArrayList<>();
var turkeyAndCheddar = new Sandwich(2, 2, true);
var grilledCheese = new Sandwich(0, 4, false);
var bigTurkeyAndCheddar = new Sandwich(10, 10, true);
var theWisconsinFreak = new Sandwich(0, 20, true);

sandwiches.add(turkeyAndCheddar);
sandwiches.add(grilledCheese);
sandwiches.add(bigTurkeyAndCheddar);
sandwiches.add(theWisconsinFreak);

for (Sandwich sandwich : sandwiches) {
    if (sandwich.mayo()) { // Some people don't like Mayo
        // But we can't get rid of them during the loop
        sandwiches.remove(sandwich);
    }
}
~   }
~}
```

If you want to remove an element at the same time as iterating over specifically an `ArrayList`, you
can get creative with indexes and regular loops.[^remove]

```java
~import java.util.ArrayList;
~
record Sandwich(
    int turkeySlices,
    int cheeseSlices,
    boolean mayo
) {}

~class Main {
~   void main() {
ArrayList<Sandwich> sandwiches = new ArrayList<>();
var turkeyAndCheddar = new Sandwich(2, 2, true);
var grilledCheese = new Sandwich(0, 4, false);
var bigTurkeyAndCheddar = new Sandwich(10, 10, true);
var theWisconsinFreak = new Sandwich(0, 20, true);

sandwiches.add(turkeyAndCheddar);
sandwiches.add(grilledCheese);
sandwiches.add(bigTurkeyAndCheddar);
sandwiches.add(theWisconsinFreak);

for (int i = 0; i < sandwiches.size(); i++) {
    Sandwich sandwich = sandwiches.get(i);
    if (sandwich.mayo()) { // Some people don't like Mayo
        sandwiches.remove(sandwich);
        i--; // Subtracting one from our current index sycs us back up
    }
}
        
System.out.println(sandwiches);
~   }
~}
```

[^should]: The reason I say "should" is that doing the book keeping needed to know when
this has happened can be hard and not all `Iterator`s in the world will do it. The check is what we would call "best effort."

[^remove]: And, as these footnotes have alluded, there is a `.remove` method on `Iterator`. We'll cover it
later.