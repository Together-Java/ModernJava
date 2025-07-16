# Arrays

When you use a for-each loop on an array, it acts the same as the kind of for-loop
you would have written before with an explicit index.

```java
record Drink(String name, double mgCaffeinePerCup) {}

~class Main {
~    void main() {
Drink[] drinks = { 
    new Drink("Black Coffee", 95),
    new Drink("Milk", 0),
    new Drink("Green Tea", 35)
};

// This loop functions the same as the loop below
for (int i = 0; i < drinks.length; i++) {
    Drink drink = drinks[i];

    IO.println(
        drink.name()
            + " has "
            + drink.mgCaffeinePerCup()
            + "mg caffiene per cup"
        );
}

IO.println("------------------");

for (Drink drink : drinks) {
    IO.println(
        drink.name()
            + " has "
            + drink.mgCaffeinePerCup()
            + "mg caffiene per cup"
        );
}
~    }
~}
```

This doesn't mean that the old style of for loop is useless now. You will still want that
if you need to know which element in your array you are dealing with
or if you are doing a more interesting form of iteration.

```java
record Drink(String name, double mgCaffeinePerCup) {}

~class Main {
~    void main() {
Drink[] drinks = { 
    new Drink("Black Coffee", 95),
    new Drink("Milk", 0),
    new Drink("Green Tea", 35)
};


// If loop actually cares to use `i` beyond just accessing
// the right element in the array
for (int i = 0; i < drinks.length; i++) {
    Drink drink = drinks[i];

    // Which you might want for display logic
    IO.println(
        "[" + i + "]: " + drink.name()
    );

    // Or to mutate the original array
    drinks[i] = new Drink(
        drink.name(),
        drink.mgCaffeinePerCup() + 100
    );
}
~    }
~}
```