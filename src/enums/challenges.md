# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Make an enum named `Response` which 
has three variants. `YES`, `NO`, and `MAYBE_SO`.

```java,editable
// -------------
// CODE HERE
// -------------

void main() {
    System.out.println(
        Response.YES
    );

    System.out.println(
        Response.NO
    );

    System.out.println(
        Response.MAYBE_SO
    );
}
```

## Challenge 2.

Write a method named `goodPerformer` which takes 
in a `String` representing the name of an artist.

If that `String` is equal to `Pitbull` or `Billy Joel`
return `YES`. If it is equal to `Shaggy` return `NO`.
Otherwise return `MAYBE_SO`.

Use the enum you defined above.

```java
// ------------
// CODE HERE
// ------------

void main() {
    Response pitbull = goodPerformer("Pitbull");
    System.out.println(pitbull);

    Response billyJoel = goodPerformer("Billy Joel");
    System.out.println(billyJoel);

    Response shaggy = goodPerformer("Shaggy");
    System.out.println(shaggy);

    Response chappelRoan = goodPerformer("Chappell Roan");
    System.out.println(chappelRoan);
}
```

## Challenge 3.

Make a method named `transition` which takes in a `StopLight`
and returns the next light it will transition to.

For those who don't drive cars: red lights go to green,
green lights go to yellow, and yellow lights go to red.

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
    System.out.println(light);

    light = transition(light);
    System.out.println(light);

    light = transition(light);
    System.out.println(light);

    light = transition(light);
    System.out.println(light);

    light = transition(light);
    System.out.println(light);

    light = transition(light);
    System.out.println(light);

    light = transition(light);
    System.out.println(light);
}
```