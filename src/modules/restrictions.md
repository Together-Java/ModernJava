# Restrictions

All classes within a module must be in named packages

Unlike packages, where two packages can have classes of the same name,
two modules cannot contain the same package. 

This means that you cannot have a class in the `java.lang` package defined
in any of your modules, as that already comes with Java. 

If you accidentally make a situation where one package is in multiple modules
we call that having a "split package" and Java will raise an error.