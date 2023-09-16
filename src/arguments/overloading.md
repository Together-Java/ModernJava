# Overloading

Multiple methods can be declared that have the same name.
This is allowed so long as each method takes different types
or different numbers of arguments.

Let's say you're a chef, you want to make a sandwich. You know multiple ways to make sandwich, maybe a basic sandwich? add some more filling etc
```java
void makeSandwich() {
    System.out.println("makes a basic sandwich");
}

void makeSandwich(String ingredientOne) {
    System.out.println("makes a sandwich with added ingredientOne");
}

void makeSandwich(String ingredient1, String ingredient2, String ingredient3) {
    System.out.println("makes a sandwich with ingredient1, ingredient2 and ingredient3");
}
```

When you call the method, Java will know what code to run
because it knows the types of and number of arguments
you are passing.

```java
void main() {
    // Java can figure out what to do
    makeSandwich();
    makeSandwich("Lettuce");
    makeSandwich("Lettuce","tomato","Onion");
}
```

When there are multiple methods that have the same name but take different arguments,
those methods are considered "overloads" of eachother[^overload]

Note: You can have as many methods you want with same name as long as each has at least one different arguement.

[^overload]:
    "Overloading" in this context means when one word has more than
    one possible meaning depending on how it is used. Buffalo buffalo Buffalo buffalo buffalo buffalo Buffalo buffalo.
