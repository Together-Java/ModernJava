# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

The following classes are named "wrong." Name them correctly.

```java,editable
class gonzo {}

class fozzie_the_bear {}

class MSPIGGY {}

void main() {
    System.out.println(new gonzo());
    System.out.println(new fozzie_the_bear());
    System.out.println(new MSPIGGY());
}
```

## Challenge 2.

Make a variable named `movie` which is an instance of the `Movie` class.
Set the value of its `title` field to `Muppets in Space`.

```java,editable
class Movie {
    String title;
}

void main() {
    // ---------------
    // CODE HERE
    // ---------------

    System.out.println(
        movie.title
    );
}
```

## Challenge 3.

Alter the `ThemePark` class so that the default value
for its `entranceFee` field is `35.24`.

```java,editable
class ThemePark {
    double entranceFee;
}

void main() {
    ThemePark themePark = new ThemePark();

    System.out.println(
        themePark.entranceFee
    );
}
```

## Challenge 4.

Changing only the indicated line,
make it so the word `Kermit` only appears twice in the
program.

Hint: Remember that inferred types exist.

```java,editable
class Kermit {
    boolean angry = true;
}

void main() {
    // ------------------------
    // CHANGE ONLY THIS LINE v
    Kermit kermit = new Kermit();
    // ------------------------

    System.out.println(kermit.angry);
}
```

## Challenge 5.

Make a method named `squareRoot` which returns an
instance of the `SquareRoot` class containing both
the `positiveRoot` and `negativeRoot` of the given `double`.

So if you are given `4` you should return a positive root
of `2` and a negative root of `-2`.

You do not have to account for the possibility of being given a negative
number. You should use `Math.sqrt` to find the positive root and common
sense to find the negative root.

```java,editable
class SquareRoot {
    double positiveRoot;
    double negativeRoot;
}

SquareRoot squareRoot(double value) {
    // -----------
    // CODE HERE
    // -----------
}

void main() {
    SquareRoot sqrtOfFour = squareRoot(4);
    // 2
    System.out.println(sqrtOfFour.positiveRoot);
    // -2
    System.out.println(sqrtOfFour.negativeRoot);

    SquareRoot sqrtOfFifteen = squareRoot(15);
    // 3.872983346207417
    System.out.println(sqrtOfFifteen.positiveRoot);
    // -3.872983346207417
    System.out.println(sqrtOfFifteen.negativeRoot);
}
```

## Challenge 6.

Only writing code between the lines and without directly accessing any fields on or reassigning the `actor` variable, make the program output `Tim Curry`.

Hint: The key word is "directly."

```java,editable
class Actor {
    String name;
}

void main() {
    Actor actor = new Actor();
    actor.name = "Frog, Kermit the";

    // --------------------------
    // CODE HERE
    // --------------------------

    System.out.println(actor.name);
}
```