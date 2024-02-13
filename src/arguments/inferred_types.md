# Inferred Types

With variable declarations, you can use `var` to let Java figure out the type
of the variable.

```java,no_run
var name = "Jupiter";
```

This is _not_ allowed with argument declarations.

```java,does_not_compile,no_run
// You aren't allowed to use var for arguments!
void makeHorchata(var milkFatPercent) {
    // ...
}
```

You must always explicitly write out the types of arguments.

```java,no_run
void makeHorchata(double milkFatPercent) {
    System.out.println(
        "Making a horchata with " + milkFatPercent + "% milk."
    );
}
```
