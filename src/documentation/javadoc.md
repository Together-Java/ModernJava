# javadoc

The way to take code with documentation comments and produce a documentation website
is with the `javadoc` tool.

There are multiple ways to run this[^theme], but if you have your code in the
multi-module directory layout you can use `--module-path` and `--module` the
same as `javac` does.

```bash,no_run
javadoc \
    -d output/javadoc \
    --module-source-path "./*/src" \
    --module one.piece
```

This will produce a directory full of HTML files that contain all
the documentation from the specified modules.

This is what is used to make [the official Java documenation](https://docs.oracle.com/en/java/javase/25/docs/api/index.html) as well as at least part of the documentation for most Java libraries.

[^theme]: As is a theme with command-line tools