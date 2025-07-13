# Check if blank

You can check if a `String` is blank by using the `.isBlank` method.

The difference is that an empty `String` has actually zero characters. A blank `String` can have characters, so long as those characters are what we would consider whitespace.
That is, things like spaces and newlines.

```java
void main() {
    String brainSounds = """
              
             

        """;

    // false
    System.out.println(brainSounds.isEmpty());

    // true
    System.out.println(brainSounds.isBlank());
}
```