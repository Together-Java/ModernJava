# Get a Method

To get a specific method from a class you can use `getMethod`. If there is no method that matches the name and argument types a `NoSuchMethodException` will be thrown. [^nosuchmethod]

```java
import java.lang.reflect.Method;

class Main {
    void main() throws NoSuchMethodException {
        Class<Tea> teaClass = Tea.class;

        Method sipMethod = teaClass.getMethod("sip");
        System.out.println(sipMethod);
    }
}

class Tea {
    public void sip() {
    }
}
```


Unlike fields which can be identified only by their name, methods which are distinct overloads of eachother
are distinguised by the arguments they take in.

```java
import java.lang.reflect.Method;

class Main {
    void main() throws NoSuchMethodException {
        Class<Tea> teaClass = Tea.class;

        // There is a sip method which takes zero arguments
        Method sipMethod = teaClass.getMethod("sip");
        System.out.println(sipMethod);
        
        // which is a different method than
        // sip that takes one int
        sipMethod = teaClass.getMethod("sip", int.class);
        System.out.println(sipMethod);
        
        // which is a different method than
        // sip that takes a String and an int
        sipMethod = teaClass.getMethod("sip", String.class, int.class);
        System.out.println(sipMethod);
    }
}

class Tea {
    public void sip() {
    }

    public void sip(int numberOfSips) {
    }

    public void sip(String baristaName, int numberOfSips) {
    }
}
```

And, as you might imagine, `getDeclaredMethod` will do the same thing with the distinction
of seeing non-public methods.

```java
class Main {
    void main() throws NoSuchMethodException {
        Class<Fruit> fruitClass = Fruit.class;

        System.out.println(fruitClass.getDeclaredMethod("bite"));
        System.out.println(fruitClass.getDeclaredMethod("chew"));
        System.out.println(fruitClass.getDeclaredMethod("swallow"));
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

