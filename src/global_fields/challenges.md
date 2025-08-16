# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

Write a method named `anothaOne`. Each time this method is 
called it should return a number one larger than the last time
it was called.

`anothaOne` should take no arguments.

```java,editable
// CODE HERE

int anothaOne() {
    // CODE HERE
}

void main() {
    IO.println(anothaOne()); // 1
    IO.println(anothaOne()); // 2
    IO.println(anothaOne()); // 3
    IO.println(anothaOne()); // 4
    IO.println(anothaOne()); // 5
}
```

## Challenge 2

Make a class named `DJKhaled`. If you ask DJ Khaleed to `produceMusic`
some lyrics should be printed out but also `anothaOne` should be called at least 7 times.[^drake]


```java,editable
// CODE FROM LAST SECTION

class DJKhaled {
    void produceMusic() {
        // CODE HERE
    }
}

void main() {
    IO.println(anothaOne()); // 1
    var dj = new DJKhaled();
    dj.produceMusic();
    IO.println(anothaOne()); // 8+, at least
}
```

## Challenge 3

Make a method named `nextLyric`. It should take no arguments and return a `String`.
Each time it is called it should return a subsequent line from [Kendrick Lamar's 2025 Superbowl 
Halftime Show](https://www.youtube.com/watch?v=KDorKy-13ak).

You should be able to find a transcription of the lyrics [here](https://genius.com/Kendrick-lamar-and-nfl-super-bowl-lix-halftime-show-lyrics).

Once all the lyrics are exhausted `nextLyric` should start returning `null`.

```java,editable
// CODE HERE

String nextLyric() {
    // CODE HERE
}

void main() {
    for (
        String lyric = nextLyric(); 
        lyric != null; 
        lyric = nextLyric()
    ) {
        IO.println(lyric);
    }
}
```

[^drake]: We are just going to have fun with the "anotha one" meme here, lets not think too hard about DJ Khaled's relationship with Drake.