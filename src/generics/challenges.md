# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt



## Challenge 1.


Will the following code work? Why or why not?

```java
class Thing<T> {
    T value;
}

class Cool {
}
class NotCool {
}

class Main {
    void main() {
        int n = Integer.parseInt(
            IO.readln("Give a number: ")
        );

        Thing<Object> o = (n % 2 == 0) 
            ? new Thing<Cool>() 
            : new Thing<NotCool>();

    }
}
```

## Challenge 2.

Make a class that holds a `NotNull` value. This class should be generic over the kind of
data that it holds but it should throw an exception if the provided `value` is `null`.

```java,editable
// CODE HERE

class Main {
    void main() {
        NotNull<String> s = new NotNull<>("abc");
        IO.println(s.value);

        NotNull<Integer> i = new NotNull<>(123);
        IO.println(i.value);

        // This should throw an exception
        // NotNull<Double> d = new NotNull<>(null);
    }
}
```


## Challenge 3.

The following class has 5 generic parameters.

Correct the ones which do not follow expected naming conventions


```java,editable
class Organism<name, h, T, Cat, inch_worm> {
    name name;
    h h;
    T t;
    Cat cat;
    inch_worm inchWorm;
}

class Main {
    void main() {
        var o = new Organism<String, Integer, Integer, String, String>();
        o.name = "abc";
        o.h = 123;
        o.t = 5;
        o.cat = "...";
        o.inchWorm = "\\_/-\\--(*)";
    }
}
```

