# Write to a Field

Similarly, you can write to a field using the `.set` method on a `Field` object.
This will also throw `IllegalAccessException` if its not something you are allowed to do.

```java
import java.lang.reflect.Field;

class Main {
    void main() throws IllegalAccessException {
        Class<Drink> drinkClass = Drink.class;

        Field caffeinatedField;
        try {
            caffeinatedField = drinkClass.getField("caffeinated");
        } catch (NoSuchFieldException e) {
            throw new RuntimeException(e);
        }

        var water = new Drink("Water", false);

        // You can put drugs in anything you set your mind to, kids
        caffeinatedField.set(water, true);

        System.out.println(caffeinatedField.get(water));
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

If you try to set a field to the wrong type of value - like setting a `boolean` field to have a `String` value -
you will get an `IllegalArgumentException`. Unlike `NoSuchFieldException` and `IllegalAccessException` this is an
unchecked exception, so you do not need to explicitly account for it.

```java
import java.lang.reflect.Field;

class Main {
    void main() throws IllegalAccessException {
        Class<Drink> drinkClass = Drink.class;

        Field caffeinatedField;
        try {
            caffeinatedField = drinkClass.getField("caffeinated");
        } catch (NoSuchFieldException e) {
            throw new RuntimeException(e);
        }

        var soda = new Drink("Soda", true);

        caffeinatedField.set(soda, "yes, very much so");

        System.out.println(caffeinatedField.get(soda));
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