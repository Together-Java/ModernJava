# Omitted Default

If you have no logic to put in it, you can omit the `default` case from a `switch`. This is the same conceptually as omitting a final `else` from a chain of `if`s and `else if`s.


```java
void react(String fruit) {
    switch (fruit) {
        case "apple" -> {
            System.out.println("WOW");
        }
        case "orange" -> {
            System.out.println("Zoinks!");
        }
        case "grape" -> {
            System.out.println("Zoopers!");
        }
    }
}

void main() {
    react("passionfruit"); // 🤷
}
```
