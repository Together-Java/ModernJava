# Naming

For static final fields people generally name them the same way you would an enum - `LIKE_THIS`.

```java
class Constants {
    static final int DAYS_IN_A_WEEK = 7;
    static final int WEEKS_IN_A_YEAR = 52;
}
```

Because you will get yelled at for using a non-final static field no matter what you do, the rules there are less strict. You can name them in all caps or like a normal variable
depending on personal preference.

```java
class Counter {
    // The people who would be mad at you for the first
    // will probably already be mad at you for the second.
    static int value = 0;
    static int VALUE = 0;
}
```