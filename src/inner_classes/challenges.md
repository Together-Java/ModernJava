# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

As written the code in `GameConsole.Controller`
looks at its own `isPoweredOn` field. 

Disambiguate the usage so that it is uses the `isPoweredOn` field from
the `GameConsole` instance wrapping it in its `status` method.

```java,editable
class GameConsole {
    boolean isPoweredOn;

    GameConsole() {
        this.isPoweredOn = false;
    }

    class Controller {
        boolean isPoweredOn;

        Controller() {
            this.isPoweredOn = false;
        }

        String status() {
            "Controller[" 
                + isPoweredOn ? "ON" : "OFF" + "] - GameConsole["
                + isPoweredOn ? "ON" : "OFF" + "]";
        }
    }
}

class Main {
    void main() {
        var console = new GameConsole();
        var controller = console.new Controller();

        IO.println(controller.status());

        console.isPoweredOn = true;
        IO.println(controller.status());

        controller.isPoweredOn = true;
        IO.println(controller.status());

        console.isPoweredOn = false;
        IO.println(controller.status());
    }
}
```

## Challenge 2.

Make the `Controller` class from the previous example a `static` inner class.
The `status` method should keep the same behavior. This means you will need
to explicitly pass an instance of `GameConsole` to the constructor of `Controller`
and store it in a field.

## Challenge 3.

Successfully make an instance of `Fly` from the `Main` class.

```java,editable
class OldLady {
    class Horse {
        class Cow {
            class Goat {
                class Dog {
                    class Cat {
                        class Bird {
                            class Spider {
                                class Fly {
                                    Fly() {
                                        IO.println("She's dead, of course");
                                    }
                                }
                            }
                        }
                    }
                }
            }
        }
    }
}

class Main {
    Fly f = /* CODE HERE */;
    IO.println(f);
}
```

## Challenge 4.

Go back to some of the programs you wrote entirely within the anonymous
main class. Turn that main class into a named class.

First make sure your program works the same as it did. Then 
go through all the inner classes in your program and mark them
as many of them as you can `static`.

Which ones can't be trivially made `static`? Note what state they
access in the enclosing instance.