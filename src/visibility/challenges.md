# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

The following `Ratio` class should have an invariant where `denominator`
cannot be `0`.

```java,no_run
class Ratio {
    int numerator;
    int denominator;

    Ratio(int numerator, int denominator) {
        if (denominator == 0) {
            throw new RuntimeException("Denominator cannot be zero");
        }
    }

    double value() {
        return ((double) numerator) / denominator;
    }
}
```

Unfortunately other classes can directly access the `denominator` field.

Make the denominator field private and add an accessor method for other classes to use.
You can name this accessor `.denominator()` or `.getDenominator()`.

## Challenge 2

Alter the code from the last challenge such that numerator is also private and only
usable via an accessor method.

## Challenge 3

Alter the code from the last challenge such that you can not only access but also
mutate the `numerator` and `denominator` fields via exposed methods.
The method for mutating the `denominator` should throw an exception
if someone tries to set it to zero.

## Challenge 4

Given this `Pineapple` class make every method except `digest` private.

```java,no_run
class Pineapple {
    void digestProtein(String name) {
        IO.println("Pineapple juice is digesting the proteins in " + name);
    }
    
    void eatPork() {
        digestProtein("pork");
    }

    void eatChicken() {
        digestProtein("chicken");
    }

    void eatBeef() {
        digestProtein("beef");
    }

    void eatYou() {
        IO.println("Pineapple juice is eating you from the inside.");
    }

    void digest(String thing) {
        switch (thing) {
            case "pork" -> eatPork();
            case "chicken" -> eatChicken();
            case "beef" -> eatBeef();
            default -> eatYou();
        }
    }
}
```

## Challenge 5

Rewrite the code from the previous challenge such that the `digest`
method on `Pineapple` does the same thing but no other private methods
exist.

Note when doing this that you wouldn't need to consider other code.
The behavior of the only exposed method does not change so those private
methods would only be "implementation details."
