# Usage

You use a static method by writing the name of the class where it is
defined followed by `.` and the method name.

```java
class StuffDoer {
    static void doStuff() {
        System.out.println("Doing stuff");
    }
}
```

```java
~class StuffDoer {
~    static void doStuff() {
~        System.out.println("Doing stuff");
~    }
~}
~
void main() {
    StuffDoer.doStuff();
}
```