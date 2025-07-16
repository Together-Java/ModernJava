# Invocation

To invoke an instance method you first need an instance of the class.

You then write `.` followed by the name of the instance method and a list of arguments.[^elmo]

```java
class Elmo {
    void talkAboutRocko() {
        IO.println("ROCKO'S NOT ALIVE!!")
    }
}

void main() {
    Elmo elmo = new Elmo();
    elmo.talkAboutRocko();
}
```

[^elmo]: Daily reminder that Elmo absolutely [hates Rocko](https://www.youtube.com/watch?v=DFBMcwaSdns)