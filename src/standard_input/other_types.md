# Other Types

Just as you can turn a `String` into an `int` using `Integer.parseInt` and you can
turn a `String` into a `double` using `Double.parseDouble`, you can use `Boolean.parseBoolean` to turn a `String` into a `boolean`.

```java,do_not_run
void main() {
    String happyString = IO.readln("Are you happy? ");
    boolean happy = Boolean.parseBoolean(happyString);
    IO.println("You are happy? " + happy);
}
```

But lest you become too comfortable, know that there is no `Character.parseCharacter` to turn a `String` into a character.
It is not always going to be the case that there is just one way to convert a `String` to any given type.

```java,do_not_run,panics
void main() {
    String gradeString = IO.readln("What is your letter grade? ");
    // Does not exist!
    char grade = Character.parseCharacter(gradeString);
    IO.println("You have a " + grade + " in the class.");
}
```