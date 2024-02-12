# Case and Default

For a switch statement you write `switch` followed by an expression in parentheses
and a list of cases in curly-braces.

Each case consists of a "case label" (`case` followed by a literal value), an arrow (`->`), and a
body to execute when the value given to the switch matches the value declared in the case. 

The final case label can just be the word `default`. This will match if none of the previous cases did
and gives you a place to put "default" behavior.

```java
void sayColor(String fruit) {
    switch (fruit) {
        case "apple" -> {
            System.out.println("Red");
        }
        case "grape" -> {
            System.out.println("Purple");
        }
        case "orange" -> {
            System.out.println("Orange");
        }
        default -> {
            System.out.println("Other");
        }
    }
}

void main() {
    sayColor("grape");
}
```