# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Replace uses of the "concrete" collection types (`ArrayList`, `HashMap`, `HashSet`)
in the following code with the corresponding collection interfaces.

You want to keep the calls like `new ArrayList` - only change how variables are typed.

```java,editable
import java.util.ArrayList;
import java.util.HashMap;
import java.util.HashSet;
import java.util.List;
import java.util.Map;
import java.util.Set;

class Main {
    void main() {
        ArrayList<String> jedi = new ArrayList<>();
        jedi.add("Luke");
        jedi.add("Anakin");
        jedi.add("Qui-Gon");
        jedi.add("Obi-Wan");

        HashSet<String> sith = new HashSet<>();
        sith.add("Palpatine");

        HashMap<String, String> winningMatchups 
            = new HashMap<>();
        winningMatchups.put("Anakin", "Palpatine");
        winningMatchups.put("Obi-Wan", "Jar-Jar");

        for (var j : jedi) {
            IO.println(j + " is a jedi");

            var matchup = winningMatchups.get(j);
            if (matchup != null) {
                if (sith.contains(matchup)) {
                    IO.println(j + " would win against " + matchup);
                }
                else {
                    IO.println(j + " would win against " + matchup + " (but they aren't sith)");
                }
            }

        }
    }
}
```

## Challenge 2.

Call `methodB` using the array returned from `methodA`.

```java
class Main {
    String[] methodA() {
        return new String[] {
            "Chewbacca",
            "Attichitcuk",
            "Mallatobuck",
            "Lumpawaroo"
        }
    }

    void methodB(List<String> character) {
        IO.println("Characters in the Star Wars Christmas Special:");
        IO.println("----------------");
        for (item : character) {
            IO.println(item);
        }
    }

    void main() {
        // CODE HERE
    }
}
```