# Relation to Delayed Assignment

Delayed assignment of variables becomes useful with `if` and `else`.

So long as Java can figure out that a variable will always be given an initial value
inside of an `if` and `else`, you will be allowed to use that variable.

```java
int age = 22;

String message;
if (age > 25) {
    message = "You might be able to rent a car";
}
else {
    message = "You cannot rent a car!";
}

System.out.println(message);
```

If it will not always be given an initial value, then you will not be allowed to
use that variable.

```java
int age = 22;

String message;
if (age > 25) {
    message = "You might be able to rent a car";
}

// message is not always given an initial value
// so you cannot use it.
System.out.println(message);
```
