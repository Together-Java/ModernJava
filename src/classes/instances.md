# Instances

Once you've declared a class, you can make an instance
of that class by saying `new` followed by that class's name
and `()`.[^var]

```java
class Muppet {

}

void main() {
    Muppet kermit = new Muppet();
    System.out.println(kermit);
}
```

Very similarly to arrays, the output from printing an instance of a class might seem like gibberish (`Main$Muppet@1be6f5c3`).
You will learn how to make it nicer later.

[^var]: I haven't used it in many code samples thus far, but if you remember `var` this is one of the times
where it can be aesthetically convenient. `var kermit = new Muppet();`
