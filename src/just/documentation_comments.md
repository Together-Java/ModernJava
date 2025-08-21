# Documentation Comments

You can describe what a recipe does by putting a `#` followed by the description
above the recipe

```justfile,no_run
# Lists available recipes
help:
    just --list

# Cleans build output
clean:
    rm -rf output

# Compiles the code
compile: clean
    javac \
        -d output/javac \
        --module-source-path "./*/src" \
        --module dan.da.dan

# Packages the code
package: compile
    jar \
        --create \
        --file output/jar/dan.da.dan.jar \
        -C output/javac/dan.da.dan .
```

These documentation comments will appear alongside the recipe name with `just --list`, which
is the command our `help` recipe runs.

```text,no_run
$ just
Available recipes:
    clean   # Cleans build output
    compile # Compiles the code
    help    # Lists available recipes
    package # Packages the code
```