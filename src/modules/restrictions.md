# Restrictions

All classes within a module must be in named packages

The packages within one module must only be in that module. This
means that you cannot have a class in the `java.lang` package defined
in any of your modules. The `java.lang` 

Unlike packages, where two packages can have classes of the same name,
two modules cannot contain the same package. 