# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Write a method named `arise` which accepts a `String` parameter
representing someone's name and prints `Awake <NAME>`.

If this function is given an empty string throw a `RuntimeException`.

```java,editable
// ------------
// CODE HERE
// ------------

void main() {
    arise("Lion El'Jonson");
    arise("Roboute Guilliman");

    arise("");
}
```

## Challenge 2.

Starting with the code you wrote above, make the thrown runtime exception
include a message saying why it was thrown ("given an empty string" or something like that.)

```java,editable
// ------------
// CODE HERE
// ------------

void main() {
    arise("Lion El'Jonson");
    arise("Roboute Guilliman");

    arise("");
}
```

## Challenge 3.

The following code is written in an intentionally confusing way.
Instead of reading the code and trying to figure it out that way,
run the code and read the stack trace to figure out which method originally
throws an exception.

```java,panics
void a(int x) {
    if (x == 0) {
        throw new RuntimeException();
    }
    else {
        b(x / 2);
    }
}

void b(int x) {
    if (x == 0) {
        throw new RuntimeException();
    }
    else {
        c(x * 3 + 5);
    }
}

void c(int x) {
    if (x == 0) {
        throw new RuntimeException();
    }
    else {
        d(x / 4);
    }
}

void d(int x) {
    if (x == 0) {
        throw new RuntimeException();
    }
    else {
        e(x / 3);
    }
}

void e(int x) {
    if (x == 0) {
        throw new RuntimeException();
    }
    else {
        a(x / 10);
    }
}

void main() {
    a(1215135236);
}
```

## Challenge 4.

Write a method named `command` which takes in a `SpaceMarine`.
If the space marine is corrupted throw a `RuntimeException`.
Otherwise print out their name.

```java,editable
class SpaceMarine {
    boolean corrupted;
    String name;
}

// ---------------------
// CODE HERE
// ---------------------

void main() {
    SpaceMarine titus = new SpaceMarine();
    titus.corrupted = false;
    titus.name = "Demetrian Titus";

    command(titus);

    SpaceMarine imurah = new SpaceMarine();
    imurah.corrupted = true;
    imurah.name = "Imurah";

    command(imurah);
}
```

## Challenge 5.

Alter your code above by adding a new method named `safeCommand`. It should
call `command` in a `try/catch` block. If a `RuntimeException` is thrown
it should print `Unable to command`.

```java,editable
class SpaceMarine {
    boolean corrupted;
    String name;
}

// ---------------------
// CODE HERE
// ---------------------

void main() {
    SpaceMarine titus = new SpaceMarine();
    titus.corrupted = false;
    titus.name = "Demetrian Titus";

    command(titus);
    safeCommand(titus);

    SpaceMarine imurah = new SpaceMarine();
    imurah.corrupted = true;
    imurah.name = "Imurah";

    safeCommand(imurah);
}
```

