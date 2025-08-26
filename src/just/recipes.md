# Recipes

A Justfile contains multiple "recipes."
These are lists of commands to run when you type `just <recipe name>`.

```justfile,no_run
help:
    just --list

compile:
    rm -rf output
    javac \
        -d output \
        --module-source-path "./*/src" \
        --module dan.da.dan
```

So in the example above `just compile` will first run `rm -rf output` followed by `javac <...>`.

The first recipe in a file is run by default when you type `just`. This is why we put
the `help` recipe first in the file - it is convenient.

```text,no_run
$ just
just --list
Available recipes:
    compile
    help
$ just help
just --list
Available recipes:
    compile
    help
```



