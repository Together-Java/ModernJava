# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

Add a static field to this `Ogre` class that keeps track of
how many Ogres have been made thus far in the program.[^threads]

```java,editable
class Ogre {
    // CODE HERE

    Ogre() {
        // CODE HERE
    }
}

class Main {
    void main() {
        // 0
        IO.println(Ogre.NUMBER_OF_OGRES_MADE);

        // 1
        Ogre o1 = new Ogre();
        IO.println(Ogre.NUMBER_OF_OGRES_MADE);

        // 2
        Ogre o2 = new Ogre();
        IO.println(Ogre.NUMBER_OF_OGRES_MADE);
        
        // 3
        Ogre o3 = new Ogre();
        IO.println(Ogre.NUMBER_OF_OGRES_MADE);
        
        // 4
        Ogre o4 = new Ogre();
        IO.println(Ogre.NUMBER_OF_OGRES_MADE);

        // 5
        Ogre o5 = new Ogre();
        IO.println(Ogre.NUMBER_OF_OGRES_MADE);
    }
}
```

## Challenge 2

Initialize the `PI` and `TAU` static final fields inside of a static initializer block.
`TAU` should have twice the value of `PI`.

```java
class Maths {
    static final double PI;
    static final double TAU;

    static {
        // CODE HERE
    }
}

class Main {
    void main() {
        IO.println(Maths.PI);
        IO.println(Maths.TAU);
    }
}
```

## Challenge 3

Rename the constants in the `Doug` class in the way that would
be expected of you by others.

```java
class Doug {
    static final String pattyMayonnaise = "Patty Mayonnaise";
    static final String sKeEtEr = "Mosquito 'Skeeter' Valentine";
    static final String mosquito_valentine = sKeEtEr;
    static final String rodgerMKlotz = "Rodger M. Klotz";
    static final String DOUG = "Douglas Yancy Funnie";
}
```


[^threads]: Part of why mutable static fields are such a nightmare is that code like this would 
not work when you have to write "multi-threaded" Java code. There are things you can do with normal fields to sort of "make unsafe stuff safe in a way," but static fields are a lot harder to wrangle.