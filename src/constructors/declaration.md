# Declaration

To declare a constructor you make a method where you don't write any return type
and whose name is the name of the class.

```java,no_run
class Muppet {
    Muppet() {

    }
}
```

Inside of the constructor's body, you can set the initial values for any fields
in the class.

```java
class Muppet {
    boolean talented;

    Muppet() {
        talented = true;
    }
}

void main() {
    Muppet gonzo = new Muppet();
    IO.println(gonzo.talented);
}
```

