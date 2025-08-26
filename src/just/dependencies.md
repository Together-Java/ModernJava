# Dependencies

If there are recipes you want to run before other recipies
you specify them after the `:` of the recipe declaration.

This can be useful for things like always removing an output
directory before compiling or packaging.

```justfile,no_run
help:
    just --list

clean:
    rm -rf output

compile: clean
    javac \
        -d output/javac \
        --module-source-path "./*/src" \
        --module dan.da.dan

package: compile
    jar \
        --create \
        --file output/jar/dan.da.dan.jar \
        -C output/javac/dan.da.dan .
```

So in the example above, all the commands in the "`compile`" recipe
run before the commands in the "`package`" recipe. Before "`compile`"
the commands in the "`clean`" recipe run.

This is useful for making these sorts of "chains" of commands, but isn't strictly required.

