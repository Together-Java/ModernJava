# Equality ignoring case

If you want to check if two `String`s contain the same contents
but you do not care if those contents differ in the casing of letters, you can use the `.equalsIgnoreCase`
method.

```java
void main() {
    String historicalFigureOne = "St. Valentines";
    String historicalFigureTwo = "st. valentines";

    IO.println(
        historicalFigureOne.equalsIgnoreCase(historicalFigureTwo)
    );
}
```

This is different from the result the `.equals` method will give you. That method will return `false` if there
are any differences in the two `String`s.