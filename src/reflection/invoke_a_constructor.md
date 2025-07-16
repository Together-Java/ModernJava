# Invoke a Constructor

Just as you can get and set a field using the `.get` and `.set` methods on a `Field` and just as you can invoke
a method by using the `.invoke` method on a `Method`, you may also
invoke constructors with `.newInstance` on a `Constructor` object.

```java
import java.lang.reflect.Constructor;
import java.lang.reflect.InvocationTargetException;

class Main {
    void main() throws
            InvocationTargetException,
            InstantiationException,
            IllegalAccessException,
            NoSuchMethodException {
        Class<AirplaneFood> airplaneFoodClass = AirplaneFood.class;
        
        Constructor<AirplaneFood> constructor
                = airplaneFoodClass.getConstructor();

        AirplaneFood airplaneFood = constructor.newInstance();
        
        IO.println(airplaneFood.tastesGood);

        constructor = airplaneFoodClass.getConstructor(boolean.class);

        airplaneFood = constructor.newInstance(false);

        IO.println(airplaneFood.tastesGood);
    }
}

class AirplaneFood {
    public final boolean tastesGood;

    public AirplaneFood() {
        this.tastesGood = false;
    }

    public AirplaneFood(boolean tastesGood) {
        if (tastesGood) {
            throw new RuntimeException("Lies");
        }
        this.tastesGood = false;
    }
}
```
