# @Retention

The next important meta-annotation is `@Retention`.

If you want to be able to access an annotation using reflection
it needs to be marked with a retention policy of `RUNTIME`.

```java,no_run
import java.lang.annotation.ElementType;
import java.lang.annotation.Retention;
import java.lang.annotation.RetentionPolicy;
import java.lang.annotation.Target;

@Target(ElementType.METHOD)
@Retention(RetentionPolicy.RUNTIME)
@interface Special {
}
```

The other two options are `SOURCE` - which will throw away any evidence of the annotation after Java
compiles your code - and `CLASS` - which will save the annotation, but not in a way you can use at runtime.

If you are making your own programs that make use of annotations, chances are you will be working with them at runtime. This means you will most likely be using `RUNTIME` more than the other options.

That being said, there is nothing particularly wrong with `SOURCE` and `CLASS`. Its just that writing programs that use the annotations at those steps require some more work and there aren't too many downsides to `RUNTIME`.