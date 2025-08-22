# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Write a method `startsWithVowel` that takes an `Object`
as input and returns if the name of the underlying
class for that `Object` starts with a vowel.

You might need to consult the documentation
for [Class](https://docs.oracle.com/en/java/javase/24/docs/api/index.html).

```java,editable
class Apple {}
class Banana {}

class Main {
    boolean startsWithVowel(Object o) {
        // CODE HERE
    }
    void main() {
        // Integer -> i -> true
        IO.println(startsWithVowel(4));


        // String -> s -> false
        IO.println(startsWithVowel("abc"));


        // Apple -> a -> true
        IO.println(startsWithVowel(new Apple()));

        // Banana -> b -> false
        IO.println(startsWithVowel(new Banana()));
    }
}
```

## Challenge 2.

Write a method `toMap` that takes an `Object`
as input and returns a `Map<String, Object>`
with all the object's field names as keys and field values
as the value.

```java,editable
class HankHill {
    public double loveForPropane = 100;
    public String shock = "bwhaaha";
}

class BobbyHill {
    public boolean hasCulinaryAcumen = true;
}

class CottonHill {
    public boolean bitter = true;
    public boolean angry = true;
    public boolean short = true;
    public boolean dead = true;
}

class Main {
    Map<String, Object> toMap(Object o) {
        // CODE HERE
    }

    void main() {
        // {loveForPropane=100, shock=bwhaaha}
        IO.println(toMap(new HankHill()));

        // {hasCulinaryAcumen=true}
        IO.println(toMap(new BobbyHill()));

        // {bitter=true, angry=true, short=true, dead=true}
        IO.println(toMap(new CottonHill()));
        
    }
}
```

## Challenge 3.

Write a method `fromMap` that takes a `Map<String, Object>`
and a `Class`
and returns an `Object` whose fields are all filled in using
the values in the map.

Assume that the given `Class` has a zero argument constructor you can
call to get an "empty" instance of the class.

Add your own `toString` methods to the example classes to debug your work.

```java,editable
class HankHill {
    public double loveForPropane;
    public String shock;

    // CODE HERE
}

class BobbyHill {
    public boolean hasCulinaryAcumen;

    // CODE HERE
}

class CottonHill {
    public boolean bitter;
    public boolean angry;
    public boolean short;
    public boolean dead;

    // CODE HERE
}

class Main {
    Object fromMap(Map<String, Object> o, Class<?> klass) {
        // CODE HERE
    }

    void main() {
        IO.println(fromMap(Map.of(
            "loveForPropane", 100,
            "shock", "bwhaaha"
        ), HankHill.class));

        IO.println(fromMap(Map.of(
            "hasCulinaryAccumen", true
        ), BobbyHill.class));

        IO.println(fromMap(Map.of(
            "bitter", true,
            "angry", true,
            "short", true,
            "dead", true
        ), CottonHill.class));
    }
}
```

## Challenge 4.

Call all the methods declared on the `Dale`
class in alphabetical order using reflection.[^speech]

Make sure not to call methods inherited from `Object`
such as `toString`, `equals`, and `hashCode`.

```java
class Dale {
    public static void u() {
        IO.println("and get yourself out of that tunnel and into some strange woman's bed!");
    }

    public static void t() {
        IO.println("wash off some of that cologne,");
    }
    
    public static void d() {
        IO.println("and the only way out is through a long dark tunnel.");
    }

    public static void f() {
        IO.println("carrying a boxcar full of heartbreak.");
    }

    public static void a() {
        IO.println("I know how dark it is for you right now");
    }

    public static void k() {
        IO.println("I'm fat and I'm old and every day I'm just going to wake up fatter and older.");
    }

    public static void q() {
        IO.println("Will I be out there next month? If I'm alive, you'd better believe it.");
    }

    public static void r() {
        IO.println("You've got to get up off that tanning bed,");
    }


    public static void g() {
        IO.println("Well let me tell you something:");
    }

    public static void h() {
        IO.println("all you can do is let it hit you and then try to find your legs.");
    }

    public static void i() {
        IO.println("I know - I've taken that hit more times than I can remember");
    }


    public static void e() {
        IO.println("And you're afraid to go in because there is a train coming at ya");
    }

    public static void j() {
        IO.println("Look at me Boomhauer.");
    }


    public static void m() {
        IO.println("I'm out there digging holes, falling into 'em, climbing out, trying again");
    }

    public static void c() {
        IO.println("You're in Hell now Boomhauer");
    }

    public static void n() {
        IO.println("And tomorrow I'm going to hang outside at a ladies' prison,");
    }

    public static void o() {
        IO.println("and the first thing those lady cons are going to see after twenty years is me.");
    }

    public static void l() {
        IO.println("Yet somehow I managed to drag this fat old bald bastard into the alley every day.");
    }

    public static void p() {
        IO.println("Will I get one? Experience says no.");
    }
    
    public static void s() {
        IO.println("slip into a tight T-shirt,");
    }
    
    public static void b() {
        IO.println("curled up lying in your own emotional vomit.");
    }
}

class Main {
    void main() {
        var dale = Dale.class;

        // CODE HERE
    }
}
```

[^speech]: https://www.youtube.com/watch?v=7nkrzI9GwNk