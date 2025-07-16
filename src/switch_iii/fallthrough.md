# Fallthrough

If the code for a given label does not have a `break` then it will "fall through"
to the cases below.

This is what makes C-style switches strange. It can occasionaly be useful if the same code should
run for some or all cases, but is annoyingly easy to do on accident.[^history] 

```java
class Main {
    void sayWhoTheyFought(String name) {
        switch (name) {
            case "Goku":
                IO.println("Fought Pilaf");
                IO.println("Fought The Red Ribbon Army");
            case "Gohan": // "Goku" will fall through to this case
                IO.println("Fought Frieza");
                IO.println("Fought Cell");
                IO.println("Fought Majin Buu");
        }
    }
    
    void main() {
        sayWhoTheyFought("Gohan");
        IO.println("----------------------");
        sayWhoTheyFought("Goku");
    }
}
```

[^history]: [This StackExchange Post](https://softwareengineering.stackexchange.com/questions/162615/why-dont-languages-use-explicit-fall-through-on-switch-statements) explains how this came about. I don't have a primary source on the "The reason that C did it that way is that the creators of C intended switch statements to be easy to optimize into a jump table." claim, but it lines up with my biases and preconceptions. Therefore it must be true!