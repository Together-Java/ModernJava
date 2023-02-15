# Concatenation

Any two strings can be concatenated by using the `+` operator.

```java
String he = "he";
String llo = "llo";

String hello = he + llo;

System.out.println(hello);
```

This will make a new `String` where the characters from the first one all appear followed by the characters in the second one.

If you try to concatenate a `String` to something that is not a `String`, like an `int` or a `double`,
then the result will be a new `String` with the characters from the "string representation" of that 
other thing.

```java
int numberOfApples = 5;
double dollahs = 1.52;

String message = "I have " + numberOfApples + 
    " apples and $" + dollahs + " in my pocket.";

System.out.println(message);
```