# Getters and Setters

A very silly thing you are likely to see if you dig around on the internet
is classes that look like this.

```java
class Person {
    private String name;
    private int age;
    
    String getName() {
        return this.name;
    }

    void setName(String name) {
        this.name = name;
    }

    String getAge() {
        return this.age;
    }

    void setAge(String age) {
        this.age = age;
    }
}
```

So people make classes with all private fields and then for each field `thing` they
have two methods - `getThing` and `setThing`.

To which you might immediately ask - what is the difference between this and just having non-private fields.

```java
class Person {
    String name;
    int age;
}
```

The answer to that is interesting. We'll get to it, but the short story is that its a bit of a holdover from a very weird period in the early 2000s.

I mention it specifically so that you know that there isn't any important information you are missing and you are not crazy.