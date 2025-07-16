# Specificity

When you write methods that accept or return collections, the social rule is to 
use the interface, not a specific collection type.

```java,no_run
// You are generally expected to write this
List<String> process(Set<Integer> elements) {
    // ...
}

// And not this
ArrayList<String> process(HashSet<Integer> elements) {
    // ...
}
```

There are valid reasons for this.

* When you take a collection as an argument
the code that follows probably would work for any implementation of that collection. Why make someone
use any specific one?
* When you return a collection it is possible you might want to change the exact kind of
collection you return later. Why make things harder for future you?

But there is also a dimension to it which is similar to how we choose to name classes, variables, and
methods. 

Socially it will cause you trouble if you make something which works in terms of a "concrete"
collection. Writing `List` instead of `ArrayList` where possible doesn't make your programs worse and it avoids frustrating interactions.