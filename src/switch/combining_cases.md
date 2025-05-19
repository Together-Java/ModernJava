# Combining Cases

If you have multiple constant values that should be handled in the same way, you can combine
case labels by separating their values with a comma.

```java
String scientificName(String vegetable) {
    switch (vegetable) {
        case "apple" -> {
            return "Malus pumila";
        }
        case "cabbage", "brussel sprouts", "kale", "cauliflower" -> {
            // Look it up. Kinda wild.
            return "Brassica oleracea";
        }
        default -> {
            return "unknown";
        }
    }
}
~
~void main() {
~    IO.println(scientificName("cabbage"));
~}
```