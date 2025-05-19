# Get all Methods


If you have a class object, you can get all the public
methods of that class using `getMethods`. This gives you
an array of `Method` objects.

Note that this will also include available methods that come from `java.lang.Object`.
In addition to `toString`, `equals`, and `hashCode` you will see a few you don't recognize.
All in due time.

```java
import java.lang.reflect.Method;

class Main {
    void main() {
        Class<Tea> teaClass = Tea.class;

        Method[] methods = teaClass.getMethods();
        for (var method : methods) {
            IO.println(method);
        }
    }
}

class Tea {
    public void sip() {
    }

    public void gulp() {
    }
}
```

Just like there is `getDeclaredFields` for seeing non-public fields, `getDeclaredMethods` will
give you all methods, regardless of their visibility.

```java
import java.lang.reflect.Method;

class Main {
    void main() {
        Class<Fruit> fruitClass = Fruit.class;

        IO.println("Using getMethods");
        Method[] publicMethods = fruitClass.getMethods();
        for (var method : publicMethods) {
            IO.println(method);
        }

        IO.println("-------------");

        IO.println("Using getDeclaredMethods");
        Method[] allMethods = fruitClass.getDeclaredMethods();
        for (var method : allMethods) {
            IO.println(method);
        }
    }
}

class Fruit {
    public void bite() {
    }

    void chew() {
    }

    private void swallow() {
    }
}
```