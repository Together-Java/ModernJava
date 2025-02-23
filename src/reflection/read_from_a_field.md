# Read from a Field

Once you have a `Field` object you can use its `get` method to read the value of that field
from an object. This will throw an `IllegalAccessException` if you try to read a field you
are not allowed to.[^permission]

```java
import java.lang.reflect.Field;

class Main {
    void main() throws IllegalAccessException {
        Class<Drink> drinkClass = Drink.class;

        Field nameField;
        try {
            nameField = drinkClass.getField("name");
        } catch (NoSuchFieldException e) {
            throw new RuntimeException(e); // Should have this field
        }

        var soda = new Drink("Soda", true);
        var water = new Drink("Water", false);

        System.out.println(nameField.get(soda));
        System.out.println(nameField.get(water));
    }
}

class Drink {
    public String name;
    public boolean caffeinated;

    Drink(String name, boolean caffeinated) {
        this.name = name;
        this.caffeinated = caffeinated;
    }
}
```

[^permission]: The rules for this go a bit beyond "you cannot read private fields."