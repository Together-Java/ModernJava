# Overloads


Just like normal methods, you can have multiple constructors so long as each constructor
takes different types or different numbers of arguments.

```java,no_run
class Muppet {
    String name;
    boolean talented;

    Muppet(String name) {
        this.name = name;
        this.talented = true;
    }

    Muppet(String name, boolean talented) {
        this.name = name;
        this.talented = talented;
    }
}
```

When you call a constructor, Java will know what code to run because it knows the types of and number of arguments you are passing.

```java
class Muppet {
    String name;
    boolean talented;

    Muppet(String name) {
        this.name = name;
        this.talented = true;
    }

    Muppet(String name, boolean talented) {
        this.name = name;
        this.talented = talented;
    }
}

void announce(Muppet muppet) {
    System.out.print(muppet.name);
    if (muppet.talented) {
        System.out.print(" is ");
    }
    else {
        System.out.print(" is not ");
    }
    IO.println("talented.");
}

void main() {
    Muppet fozzie = new Muppet("Fozzie");
    announce(fozzie);

    // Always a critic...
    Muppet waldorf = new Muppet("Waldorf", false);
    announce(waldorf);
}
```