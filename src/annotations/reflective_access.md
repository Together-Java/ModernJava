# Reflective Access

If something is annotated with a runtime retained annotation,
you can get an object holding that data using `.getAnnotation`.

This will either return `null` if the field, method, class, etc. is not
annotated with that annotation or it will give you an object
with methods you can call to see the values specified in the annotation.

```java
import java.lang.annotation.Retention;
import java.lang.annotation.RetentionPolicy;
import java.lang.reflect.Field;

class Main {
    void main() {
        Class<Drink> drinkClass = Drink.class;

        Field[] fields = drinkClass.getFields();
        for (var field : fields) {
            System.out.print(field.getName());
            System.out.print(" - ");

            Special annotationValue = field.getAnnotation(Special.class);
            if (annotationValue == null) {
                IO.println("is not special.");
            }
            else if (annotationValue.isSuperDuperSpecial()) {
                IO.println("is super-duper special.");
            }
            else {
                IO.println("is special.");
            }
        }
    }
}

@Retention(RetentionPolicy.RUNTIME)
@interface Special {
    boolean isSuperDuperSpecial() default false;
}

class Drink {
    public String name;

    @Special
    public boolean caffeinated;

    @Special(isSuperDuperSpecial = true)
    public String cost;

    public int height;
}
```

You can make use of this to implement a **very** wide variety of programs.