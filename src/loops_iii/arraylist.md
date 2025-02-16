# ArrayList

One class which implements `Iterable` is `ArrayList`.

```java
~import java.util.ArrayList;
~
~class Main {
~   void main() {
ArrayList<String> donutEaters = new ArrayList<>();
donutEaters.add("Chief Wiggum");
donutEaters.add("Homer Simpson");

Iterator<String> donutEatersIterator = donutEaters.iterator();
// Check if there is a next element
while (donutEatersIterator.hasNext()) { 
    // If there is, get it and advance the iterator
    String donutEater = donutEatersIterator.next();

    System.out.println(donutEater + " eats donuts");
}
~   }
~}
```

This means you can loop over it with a for-each loop same as an array.

```java
~import java.util.ArrayList;
~
~class Main {
~   void main() {
ArrayList<String> donutEaters = new ArrayList<>();
donutEaters.add("Chief Wiggum");
donutEaters.add("Homer Simpson");

for (String donutEater : donutEaters) {
    System.out.println(donutEater + " eats donuts");
}
~   }
~}
```