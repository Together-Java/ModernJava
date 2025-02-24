# Get a Constructor

Following the pattern, `getConstructor` gets a reference to a `Constructor` object.
Just like `getMethod`, this requires specifying argument types.

Since `getField` might throw a `NoSuchFieldException` and `getMethod` might
throw a `NoSuchMethodException` you might expect a `getConstructor` to throw
a `NoSuchConstructorException`. It does not. If there is no match for the constructor
you are trying to find it will reuse `NoSuchMethodException`.

`Constructor` objects are also similar to `Class` objects in that they can carry a generic parameter
specifying what kind of object will be made when they are invoked.

```java
import java.lang.reflect.Constructor;

class Main {
    void main() throws NoSuchMethodException {
        Class<AirplaneFood> airplaneFoodClass = AirplaneFood.class;

        // Zero argument constructor. 
        // Note that we have Constructor<AirplaneFood>. 
        // If you have a Class<?> it will give you a Constructor<?>
        Constructor<AirplaneFood> constructor
                = airplaneFoodClass.getConstructor();

        System.out.println(constructor);
        
        // One argument constructor
        constructor = airplaneFoodClass.getConstructor(boolean.class);

        System.out.println(constructor);
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