# Switch


<img src="/switch/header.png" height="200px"/>

`if` and `else` let you branch logic based on whether any arbitrary
expression that evaluates to a boolean.

This is powerful because it lets you write logic as complicated as
you need to.

```java,no_run
if (isLeapYear && !bloodMoon && (age > 30 || catName.equals("fred"))) {
    startRitual();
}
```

But it can be burdensome if all you are doing is checking if some variable has a particular value.

```java,no_run
~void main() {
if (food.equals("apple")) {
    IO.println("Red");
}
else if (food.equals("grape")) {
    IO.println("Purple");
}
else if (food.equals("orange")) {
    IO.println("Orange");
}
else {
    IO.println("Other");
}
~}
```

For these situations, you can use a `switch`.

```java,no_run
switch (fruit) {
    case "apple" -> {
        IO.println("Red");
    }
    case "grape" -> {
        IO.println("Purple");
    }
    case "orange" -> {
        IO.println("Orange");
    }
    default -> {
        IO.println("Other");
    }
}
```

