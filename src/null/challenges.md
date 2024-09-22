# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Write a method which takes in a `String[]` representing
a series of names and prints out every name in sequence.

If this method is given `null`, it should act as if it
was given an empty array.


```java,editable
void printNames(String[] names) {

}

void main() {
    printNames(new String[] {
        "Joker",
        "Batman",
        "Alfred"
    });
}
```

## Challenge 2.

Alter the method you wrote in the previous challenge
so that if it is given `null` it outputs the message 
`You do not know any names yet`.

If it is given an empty `String[]` it should continue
to simply output nothing.

```java,editable
void printNames(String[] names) {

}

void main() {
    printNames(new String[] {
        "Joker",
        "Batman",
        "Alfred"
    });
}
```

## Challenge 3.

Will the following code throw a `NullPointerException`?
Why or why not?

```java
void main() {
    String[] jobs = new String[] {
        "Carpenter",
        "Baker",
        null,
        "Astronomer"
    };

    for (int i = 0; i < jobs.length; i++) {
        System.out.println(jobs[i]);
    }
}
```

## Challenge 4.

The following code won't work. Give your best guess as to why
and then try running it.

```java
void main() {
    int[] numbers = new int[] {
        45,
        32,
        null,
        94
    };

    for (int i = 0; i < numbers.length; i++) {
        System.out.println(numbers[i]);
    }
}
```

## Challenge 5.

Without changing anything in the `main` method, make the `howBig`
method not throw a `NullPointerException` and still have the "correct"
behavior for non-null inputs.

```java,editable
int howBig(String letters) {
    int bigness = 0;
    for (int i = 0; i < letters.length(); i++) {
        bigness++;
    }
    return bigness;
}

void main() {
    System.out.println(
        bigness("boiler")
    );

    System.out.println(
        bigness("filter")
    );

    System.out.println(
        bigness("knower")
    );

    System.out.println(
        bigness(null)
    );
}
```