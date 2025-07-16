# Recurse Over a String

To write a recursive function which acts over each character
of a `String` you need to do much the same task as with regular loops,
just by having your "current index" be a parameter to the function.

```java
class Main {
    void printEachUpperCase(String s, int i) {
        if (i < s.length()) {
            IO.println(Character.toUpperCase(s.charAt(i)));
            printEachUpperCase(s, i + 1);
        }
    }

    void printEachUpperCase(String s) {
        printEachUpperCase(s, 0);
    }
    
    void main() {
        printEachUpperCase("hello");
    }
}
```

This overload with the index is an example of a function taking an accumulator.