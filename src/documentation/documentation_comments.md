# Documentation Comments

To document our code we can use "documentation comments."

These work the same as regular comments but instead of using two slashes (`//`)
we use three slashes (`///`).[^old]

You put these documentation comments above different elements of your program
with text describing what the purpose of those elements are.

```java
/// This class represents a ninja
public class Ninja {
    /// Says a catchphrase
    public void forsooth() {
        // ..
    }
}
```

[^old]: There is an older way to make documentation comments using `/**` and `*/` (note the extra `*` in `/**`), but we prefer this one because the way you write the actual content of the comment is easier. You are sure to see these around though.