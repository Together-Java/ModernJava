# Justfile

To use `just`, first make a file named `Justfile` and put it at the top of your project.

```text,no_run
project/
  dan.da.dan/
    src/
      module-info.java
      characters/
        MoMo.java
        JiJi.java
  Justfile
```

In this file put the following contents.

```justfile,no_run
help:
    just --list
```

This makes it so that if you run `just` or `just help`
it will list the "recipes" available for the project.