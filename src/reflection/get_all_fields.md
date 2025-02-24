# Get all Fields

If you have a class object, you can get all the public
fields of that class using `getFields`. This gives you
an array of `Field` objects.

```java
import java.lang.reflect.Field;

class Main {
    void main() {
        Class<Drink> drinkClass = Drink.class;

        Field[] fields = drinkClass.getFields();
        for (var field : fields) {
            System.out.println(field.getName());
        }
    }
}

class Drink {
    public String name;
    public boolean caffeinated;   
}
```

Its worth knowing that `getFields` will not list non-public fields. To
get a list of all fields, including private and package-private ones,
you need to use `getDeclaredFields`.

```java
import java.lang.reflect.Field;

class Main {
    void main() {
        Class<Soup> soupClass = Soup.class;

        System.out.println("Using getFields");
        Field[] publicFields = soupClass.getFields();
        for (var field : publicFields) {
            System.out.println(field.getName());
        }

        System.out.println("-------------");

        System.out.println("Using getDeclaredFields");
        Field[] allFields = soupClass.getDeclaredFields();
        for (var field : allFields) {
            System.out.println(field.getName());
        }
    }
}

class Soup {
    public String name;
    boolean isChicken;
    private boolean hasVeggies;   
}
```