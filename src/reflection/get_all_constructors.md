# Get all Constructors

If you want a list of all constructors, `.getConstructors` will give you that.

What is worth noting is that unlike `.getConstructor` the array returned from this
will not have the generic filled in.[^genericarrays]

```java
import java.lang.reflect.Constructor;

class Main {
    void main() {
        Class<AirplaneFood> airplaneFoodClass = AirplaneFood.class;

        Constructor<?>[] constructors
                = airplaneFoodClass.getConstructors();
        
        for (Constructor<?> constructor : constructors) {
            IO.println(constructor);
        }
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

[^genericarrays]: Arrays of generic objects are, in general, a hairy topic. Java can't really ensure that you use them right,
so there a lot of restrictions on making them. You can't make an `ArrayList<String>[]`, for example. 