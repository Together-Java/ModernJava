# Instance Methods

In addition to having fields, classes can also have their own method
definitions.

These look the same as the method definitions you've
seen so far, they are just put within a class definition.[^kermitangry]

```java
class Muppet {
    String name;

    void freakOut() {
        IO.println("**ANGRY KERMIT NOISES**")
    }
}
```

We call these instance methods because you need an instance of the class in order
to call the method.

[^kermitangry]: If you haven't seen the muppets this might have go over your head,
but Kermit [randomly gets really mad.](https://www.youtube.com/watch?v=SVDgHEg2jnY)