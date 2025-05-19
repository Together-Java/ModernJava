# Challenges

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Write a `Shoe` class. Give each shoe a `name` field and a `quality` field.
Have these fields be initialized inside of a constructor.

```java,editable
enum Quality {
    SUPA_FINE,
    FINE,
    SUB_FINE
}

// CODE HERE

void main() {
    Shoe nike = new Shoe("Nikes", Quality.SUB_FINE);
    IO.println(
        "SHOE: " + nike.name + ", " + nike.quality
    );


    Shoe moccasin = new Shoe("Moccasins", Quality.SUPA_FINE);
    IO.println(
        "SHOE: " + moccasin.name + ", " + moccasin.quality
    );
}
```

## Challenge 2.

Add a new `price` field to the `Shoe` class you wrote above.

Add a new constructor which accepts a third argument to set the `price`.
Keep the old two argument constructor around as well. When that one is
used set `price` to `null`.

Hint: Use `Double` to represent a nullable price.

```java,editable
enum Quality {
    SUPA_FINE,
    FINE,
    SUB_FINE
}

// CODE HERE

void main() {
    Shoe jays = new Shoe("Air Jordans", Quality.FINE, 130.0);
    IO.println(
        "SHOE: " + jays.name + ", " + jays.quality + ", $" + jays.price
    );

    Shoe nike = new Shoe("Nikes", Quality.SUB_FINE, 25);
    IO.println(
        "SHOE: " + nike.name + ", " + nike.quality + ", $" + jays.price
    );


    Shoe moccasin = new Shoe("Moccasins", Quality.SUPA_FINE);
    IO.println(
        "SHOE: " + moccasin.name + ", " + moccasin.quality + ", $" + jays.price
    );
}
```

## Challenge 3.

Alter the `Shoe` class so that the `price` field is final.
Alter its constructors so that if they are given a negative
value they throw an exception instead of finishing normally.

Keep in mind that while `null` is allowed (you might not know the price)
a negative number wouldn't be. Nobody is paying you to take their shoes.[^holes]

```java,editable
enum Quality {
    SUPA_FINE,
    FINE,
    SUB_FINE
}

// CODE HERE

void main() {
    Shoe jays = new Shoe("Air Jordans", Quality.FINE, 130.0);
    IO.println(
        "SHOE: " + jays.name + ", " + jays.quality + ", $" + jays.price
    );

    Shoe nike = new Shoe("Nikes", Quality.SUB_FINE, 25);
    IO.println(
        "SHOE: " + nike.name + ", " + nike.quality + ", $" + jays.price
    );


    Shoe moccasin = new Shoe("Moccasins", Quality.SUPA_FINE);
    IO.println(
        "SHOE: " + moccasin.name + ", " + moccasin.quality + ", $" + jays.price
    );

    Shoe shouldCrash = new Shoe("Base Ball Cleats", Quality.SUPA_FINE, -10);
}
```

[^holes]: If they do, you are going to dig holes in the desert in search of treasure that rightfully belongs
to you.

## Challenge 4.

If you haven't yet, rewrite your `Shoe` constructors so only one of them actually sets fields
and the other just delegates to that one.

```java,editable
enum Quality {
    SUPA_FINE,
    FINE,
    SUB_FINE
}

// CODE HERE

void main() {
    Shoe jays = new Shoe("Air Jordans", Quality.FINE, 130.0);
    IO.println(
        "SHOE: " + jays.name + ", " + jays.quality + ", $" + jays.price
    );

    Shoe nike = new Shoe("Nikes", Quality.SUB_FINE, 25);
    IO.println(
        "SHOE: " + nike.name + ", " + nike.quality + ", $" + jays.price
    );


    Shoe moccasin = new Shoe("Moccasins", Quality.SUPA_FINE);
    IO.println(
        "SHOE: " + moccasin.name + ", " + moccasin.quality + ", $" + jays.price
    );

    Shoe shouldCrash = new Shoe("Base Ball Cleats", Quality.SUPA_FINE, -10);
}
```