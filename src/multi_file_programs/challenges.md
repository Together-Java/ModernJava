# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

Put this code in a file named `Pickle.java`

```java
class Pickle {
    boolean dill;
}
```

Put this code in a file named `Ramen.java`

```java
class Ramen {
    void mixWith(Pickle pickle) {
        IO.println("This is gross.");
        if (pickle.dill) {
            IO.println("Extra super gross.");
        }
    }
}
```

And finally put this code in `Main.java`

```java
class Main {
    void main() {
        var pickle = new Pickle();
        pickle.dill = true;

        var ramen = new Ramen();

        ramen.mixWith(pickle);
    }
}
```

Then run the entire program from your terminal by using `java Main.java`
in the directory where you made these files.

## Challenge 2

Move `Ramen.java`, `Pickle.java`, and `Main.java` into a folder named `src`.

Make sure you can still run the program by typing `java src/Main.java`.

## Challenge 3

The following code uses an anonymous main class. Make it instead use a named class.

```java,editable
int dogs = 99;

void main() {
    while (dogs > 0) {
        IO.println(dogs + " dogs on the floor.");
        IO.println("Wake one up, take it for a walk");
        dogs--;
    }
    IO.println("No more dogs on the floor.");
}
```

## Challenge 4


Combine the following programs while keeping them in separate files.
This will require you to give names to both classes as well as
parameterize the "dogs on the floor" program in some way.

```java
int dogs = 99;

void main() {
    while (dogs > 0) {
        IO.println(dogs + " dogs on the floor.");
        IO.println("Wake one up, take it for a walk");
        dogs--;
    }
    IO.println("No more dogs on the floor.");
}
```


```java
void main() {
    while (true) {
        try {
            int dogs = Integer.parseInt(IO.readln("How many dogs are on the floor? "));
            IO.println("TODO"); // Call the first program here somehow.
        } catch (RuntimeException e) {
            IO.println("Goodbye!");
        }
    }
    
}
```