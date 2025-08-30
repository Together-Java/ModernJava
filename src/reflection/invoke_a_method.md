# Invoke a Method

Just as you can get and set a field using the `.get` and `.set` methods on a `Field`, you can invoke
a method by using the `.invoke` method on a `Method`.


For instance methods there is a first "hidden" argument that is the instance you would be invoking the method on.
This needs to be the first argument to `.invoke`.

```java
import java.lang.reflect.InvocationTargetException;
import java.lang.reflect.Method;

class Main {
    void main() throws IllegalAccessException, InvocationTargetException {
        Class<Tea> teaClass = Tea.class;

        // sip taking zero arguments
        Method sipMethod;
        try {
            sipMethod = teaClass.getMethod("sip", int.class);
        } catch (NoSuchMethodException e) {
            throw new RuntimeException(e);
        }

        var tea = new Tea();

        sipMethod.invoke(tea, 5);
    }
}

class Tea {
    public void sip(int numberOfSips) {
        IO.println("You made " + numberOfSips + " sips");
    }
}
```

For static methods you do not need an instance of the class to invoke them.
Instead, the first argument is ignored. You can pass `null`.

```java
import java.lang.reflect.InvocationTargetException;
import java.lang.reflect.Method;

class Main {
    void main() throws IllegalAccessException, InvocationTargetException {
        Class<Apple> appleClass = Apple.class;

        // sip taking zero arguments
        Method biteMethod;
        try {
            biteMethod = appleClass.getMethod("bite", int.class);
        } catch (NoSuchMethodException e) {
            throw new RuntimeException(e);
        }

        biteMethod.invoke(null, 5);
        biteMethod.invoke(null, 1);
    }
}

class Apple {
    public static void bite(int times) {
        IO.println("You took " + times + " bite" + (times < 1 ? "." : "s."));
    }
}
```