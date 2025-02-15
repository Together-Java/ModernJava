# yield

If every branch of a C-style switch `yield`s a value, you can use that switch as an expression.

```java
enum Technique {
    KAMEHAMEHA,
    INSTANT_TRANSMISSION,
    KAIOKEN,
    ULTRA_INSTINCT
}

class Main {
    boolean didGokuStealItFromSomeoneElse(Technique technique) {
        boolean answer = switch (technique) {
            case KAMEHAMEHA:
            case INSTANT_TRANSMISSION:
            case KAIOKEN:
                yield true;
            case ULTRA_INSTINCT:
                yield false;
        };
        
        return answer;
    }

    void main() {
        System.out.println(
                didGokuStealItFromSomeoneElse(Technique.INSTANT_TRANSMISSION)
        );
    }
}
```

In this situation you do not need to have a `default` case for switches over enums. Java will believe that
you covered every possibility.