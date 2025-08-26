# Class Files

The format that the Java compiler outputs is called a "class file."

These class files are what is loaded into the "Java Virtual Machine" to actually run your program. This is
in part because the Java Virtual Machine was conceived as a general tool not technicially specific to Java.

There are other languages besides Java - such as [Clojure](https://clojure.org/) and [Kotlin](https://kotlinlang.org/) - which
also can be compiled into class files. 

```text

Java Source Code --> javac -------------\
                                         ----> Class Files --> Java Virtual Machine
Kotlin Source Code --> kotlinc ---------/  |
                                          /
Lombok Source Code --> lombokc ----------/

... and more
```

This lets those languages make use of the Java Virtual Machine and all the millions
of dollars and decades of work put into making it run code fast.[^bringup]

[^bringup]: I bring this up because if you are only thinking about Java it might seem like a
pointless extra step. It somewhat is, but at the same time it lets other languages "compete"
on more or less even ground. The JVM is a labor of fill-in-the-blank, that is for sure.