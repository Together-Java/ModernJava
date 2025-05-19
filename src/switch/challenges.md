# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Write a method named `isSorcerer`. If the method is given
any of `"yuji"` or `"gojo"` return `true`. Otherwise return `false`.

Start by writing this with `if` and `else`. Then alter the code so it uses
`switch` instead.

```java
boolean isSorcerer(String name) {
    // CODE HERE
}

void main() {
    IO.println(
        isSorcerer("yuji")
    );

    IO.println(
        isSorcerer("gojo")
    );

    IO.println(
        isSorcerer("yugi") // Wrong series
    );
}
```

## Challenge 2.

Same basic challenge as above, but write a method named `didRedSoxWin`
which takes an `int` representing a year.

Return `true` if that is a year the Boston Red Sox won a world series.
`false` otherwise. This time start off by using a switch.

```java
boolean didRedSoxWin(int year) {
    // CODE HERE
}

void main() {
    IO.println(
        "2004: " + didRedSoxWin(2004)
    );

    IO.println(
        "1998: " + didRedSoxWin(1998)
    );

    IO.println(
        "2013: " + didRedSoxWin(2013)
    );

    IO.println(
        "1903: " + didRedSoxWin(1903)
    );
}
```


## Challenge 3.

Make a method named `transition` which takes in a `StopLight`
and returns the next light it will transition to.

For those who don't drive cars: red lights go to green,
green lights go to yellow, and yellow lights go to red.

This is a duplicate of a challenge from a previous section. This time
do it using a `switch`.

```java,editable
enum StopLight {
    RED,
    YELLOW,
    GREEN
}

StopLight transition(StopLight current) {
    // ------------
    // CODE HERE
    // ------------
}

void main() {
    var light = StopLight.RED;
    IO.println(light);

    light = transition(light);
    IO.println(light);

    light = transition(light);
    IO.println(light);

    light = transition(light);
    IO.println(light);

    light = transition(light);
    IO.println(light);

    light = transition(light);
    IO.println(light);

    light = transition(light);
    IO.println(light);
}
```

## Challenge 4.

In reality a `StopLight` can also be broken and not function
at all. Alter `transition` so it accounts for a new `BROKEN`
state which transitions to itself. (`BROKEN` goes to `BROKEN`).

```java,editable
enum StopLight {
    RED,
    YELLOW,
    GREEN,
    BROKEN
}

StopLight transition(StopLight current) {
    // ------------
    // CODE HERE
    // ------------
}

void main() {
    var light = StopLight.RED;
    IO.println(light);

    light = transition(light);
    IO.println(light);

    light = transition(light);
    IO.println(light);

    light = transition(light);
    IO.println(light);

    light = transition(light);
    IO.println(light);

    light = transition(light);
    IO.println(light);

    light = transition(light);
    IO.println(light);
}
```

## Challenge 5.

Given a type of bear, return the correct course of action
if you run into one in the wild and it attacks you.

If the bear is `null`, return `null` as the action to take.

If you don't know what to do when you run into a bear, look it up. Use `switch`
first then try writing the same logic using `if` and `else`.

```java
enum Bear {
    POLAR,
    BROWN,
    BLACK,
    PANDA,
    KOALA
}

enum Action {
    LAY_DOWN,
    FIGHT_BACK,
    RUN_AWAY
    YEET
}

Action inCaseOfBearAttack(Bear bear) {
    // CODE HERE
}

void main() {
    IO.println(
        inCaseOfBearAttack(Bear.POLAR)
    );

    IO.println(
        inCaseOfBearAttack(Bear.BROWN)
    );


    IO.println(
        inCaseOfBearAttack(Bear.BLACK)
    );

    IO.println(
        inCaseOfBearAttack(Bear.PANDA)
    );

    IO.println(
        inCaseOfBearAttack(Bear.KOALA)
    );

    IO.println(
        inCaseOfBearAttack(null)
    );
}
```