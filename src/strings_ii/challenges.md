# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Write a method named `isUpperCase` which tells you if a
given `String` is already made of all upper-case characters.

Hint: One way to do this is to call `.toUpperCase` and check
if the result is the same as the input you were given.

```java,editable
boolean isUpperCase(String s) {
    // -----------
    // CODE HERE
    // -----------
}

void main() {
    // true
    System.out.println(isUpperCase("ABC"));
    // false
    System.out.println(isUpperCase("abc"));
    // false
    System.out.println(isUpperCase("AbC"));
}
```

## Challenge 2.

Do the same as above, but check if a given `String` is
made of all lower case letters.

```java,editable
boolean isLowerCase(String s) {
    // -----------
    // CODE HERE
    // -----------
}

void main() {
    // false
    System.out.println(isLowerCase("ABC"));
    // true
    System.out.println(isLowerCase("abc"));
    // false
    System.out.println(isLowerCase("AbC"));
}
```

## Challenge 3.

Add an instance method named `scream` to the `Muppet` class. This
should replace the name of the muppet with the name in upper case
letters + an exclamation point (`!`) at the end.

```java,editable
class Muppet {
    String name;

    // -------------
    // CODE HERE
    // -------------
}

void main() {
    var kermit = new Muppet();
    kermit.name = "kermit";

    // kermit
    System.out.println(kermit.name);

    // KERMIT!
    kermit.scream();
    System.out.println(kermit.name);
}
```

## Challenge 4.

Write a method called `echo`.

If `echo` is given a non-blank `String`, it should print `You Said: <...>` 
where `<...>` is the `String` they
gave minus any leading or trailing whitespace.

If `echo` is given a `blank` `String`, it should print `You Didn't Say Anything`.

```java,editable
void echo(String s) {
    // -------------
    // CODE HERE
    // -------------
}

void main() {
    // You Said: Hello
    echo("Hello");

    // You Said: Hello
    echo("        Hello         ");

    // You Didn't Say Anything
    echo("");

    // You Didn't Say Anything
    echo("                ");
}
```