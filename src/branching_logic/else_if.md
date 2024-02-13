# Else If

If you have an `if` nested in an `else` branch, you can simplify that by using
`else if`.

```java
~void main() {
boolean cool = true; // 🕶️
int age = 30; // 🙎‍♀️
if (age < 25) {
    System.out.println("You cannot rent a car!");
}
else {
    if (!cool) {
        System.out.println("You failed the vibe check.");
    }
    else {
        System.out.println("You are rad enough to rent a car.");
    }
}
~}
```

So the following will work the same as the code above.

```java
~void main() {
boolean cool = true; // 🕶️
int age = 30; // 🙎‍♀️

if (age < 25) {
    System.out.println("You cannot rent a car!");
}
else if (!cool) {
    System.out.println("You failed the vibe check.");
}
else {
    System.out.println("You are rad enough to rent a car.");
}
~}
```

You can have as many `else if`s as you need. Each one will only run if all the previous conditions
evaluate to `false`.

```java
~void main() {
boolean cool = true; // 🕶️
int age = 100; // 👴

if (age < 25) {
    System.out.println("You cannot rent a car!");
}
else if (!cool) {
    System.out.println("You failed the vibe check.");
}
else if (age > 99) {
    System.out.println("You are too old to safely drive a car!");
}
else if (age > 450) {
    System.out.println("There can only be one! ⚔️🏴󠁧󠁢󠁳󠁣󠁴󠁿");
}
else {
    System.out.println("You are rad enough to rent a car.");
}
~}
```
