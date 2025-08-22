# Derived Values

A common use for methods is to provide a value that is derived from
the values of other fields.

```java
class Elmo {
    int age;

    int nextAge() {
        return age + 1;
    }
}

void main() {
    Elmo elmo = new Elmo();
    elmo.age = 3;

    IO.println("Elmo is " + elmo.age + " right now,");
    IO.println("but next year Elmo will be " + elmo.nextAge());
}
```

Which is useful for situations like where you store someones first and last name
but need to ask "what is their full name?"

```java
class Elmo {
    String firstName;
    String lastName;

    String fullName() {
        return firstName + " " + lastName;
    }
}

void main() {
    Elmo elmo = new Elmo();
    elmo.firstName = "Elmo";
    elmo.lastName = "Furchester";

    IO.println("Elmo's full name is " + elmo.fullName());
}
```