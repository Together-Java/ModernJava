# Declaration

To declare a module, you need to create a file named `module-info.java`
and put it at the top of the folder where your code is.

```
src/
  example/
    Example.java
  some/
    packageName/
      AClass.java
  module-info.java
```

Within this file you put `module` followed by a name for the grouping of packages and `{}`.[^itsbest]

```java
module example {
}
```

Just like with package names, module names can have multiple parts separated by `.`s.

```java
module a.longer.name {
}
```

Nothing in this declaration says explicitly what packages are part of the module; it is just assumed that it holds the packages it is "next to."

[^itsbest]: This name doesn't need to be related to the names of the packages, but whenever possible it's best to pick something that makes sense