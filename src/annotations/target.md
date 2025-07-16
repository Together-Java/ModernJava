# @Target

Annotations can mark most parts of your program. Annotations are a part of your program.
Therefore annotations can have annotations.

The first of these "meta-annotations" you are likely to use is `@Target`.
By default an annotation can mark anything, but you can use `@Target` to
restrict what can be marked.[^typeuse]

```java
import java.lang.annotation.ElementType;
import java.lang.annotation.Target;

// @Even can now only be used on fields and methods,
// but not classes
@Target({
        ElementType.FIELD, 
        ElementType.METHOD
})
@interface Even {
}
```

[^typeuse]: The exception to this is the `TYPE_USE` target. That one needs to be explicitly specified.