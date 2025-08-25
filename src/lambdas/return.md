# Return


If the method on the functional interface has a return value
that is not `void` you can return a value from a lambda
the same as from a method.

This will not return from any enclosing method.

```java
@FunctionalInterface
interface Farmer {
    String farm(String item);
}

class Main {
    void main() {
        Farmer jeremyClarkson = item -> {
            if (Math.random() < 0.1) {
                return "failure";
            }
            else {
                return item;
            }
        };

        IO.println(jeremyClarkson.farm("potato"));
        IO.println(jeremyClarkson.farm("sheep"));
    }
}
```

If the value is returned by a single expression you
do not need `return` or `{}`.

```java
@FunctionalInterface
interface Farmer {
    String farm(String item);
}

class Main {
    void main() {
        Farmer caleb = item -> item;

        IO.println(caleb.farm("potato"));
        IO.println(caleb.farm("sheep"));

        caleb = item -> item.toUpperCase();
        
        IO.println(caleb.farm("potato"));
        IO.println(caleb.farm("sheep"));
    }
}
```

