# Get a Field

You can retrieve a single field by its name using `getField`. If there
is no field with that name it will throw a `NoSuchFieldException`.

```java
import java.lang.reflect.Field;

class Main {
    void main() throws NoSuchFieldException {
        Class<Drink> drinkClass = Drink.class;

        Field nameField = drinkClass.getField("name");
        System.out.println(nameField);
    }
}

class Drink {
    public String name;
    public boolean caffeinated;
}
```

And if you need to access a field that might be non-public you can use `getDeclaredField`.

```java,panics
import java.lang.reflect.Field;

class Main {
    void main() throws NoSuchFieldException {
        Class<Soup> soupClass = Soup.class;

        Field hasVeggiesField = soupClass.getDeclaredField("hasVeggies");
        System.out.println(hasVeggiesField);
        
        // Will fail. getField won't see hasVeggies
        soupClass.getField("hasVeggies");
    }
}

class Soup {
    public String name;
    boolean isChicken;
    private boolean hasVeggies;
}
```

