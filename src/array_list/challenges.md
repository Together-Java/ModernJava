# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Replace at least one custom usage of a growable array in the code you have written so far
with an `ArrayList`.

## Challenge 2.

Capitalize every `String` in the `ArrayList<String>`.


```java
class Main {
    void main() {
        ArrayList<String> things = new ArrayList<>();
        things.add("movies");
        things.add("television");
        things.add("video games");
        
        // CODE HERE

        // Should output
        // [MOVIES, TELEVISION, VIDEO GAMES]
        IO.println(things); 
    }
}
```

## Challenge 3.

Every time John Wick assassinates someone he gets one crime coin
(to spend at a crime hotel).

Watch the first John Wick movie. For each named character you can remember
John Wick assassinating add one crime coin to the `johnWick` ArrayList.

```java
record CrimeCoin(String target) {}

class Main {
    void main() {
        ArrayList<CrimeCoin> johnWick = new ArrayList<>();
        
        // CODE HERE

        IO.println(johnWick);
    }
}
```

If you need to cheat you can find [the list here](https://listofdeaths.fandom.com/wiki/John_Wick#John_Wick_(2014)).

## Challenge 4.

Using the `ArrayList` of `CrimeCoin`s, construct an `ArrayList<String>` with all the characters'
names.

```java
record CrimeCoin(String target) {}

class Main {
    void main() {
        ArrayList<CrimeCoin> johnWick = new ArrayList<>();
        
        // CODE FROM LAST CHALLENGE

        ArrayList<String> names = new ArrayList<>();

        // CODE HERE

        IO.println(names);
    }
}
```

