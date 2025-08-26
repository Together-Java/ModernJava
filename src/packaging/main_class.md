# --main-class

When making a JAR you can specify a "main class"
for that JAR using the `--main-class` flag.

```bash,no_run
jar \
    --create \
    --file ex.mod.jar \
    --main-class some.pkg.Main \
    -C output/ex.mod .
```

This makes it so that you can run the code in a JAR without knowing which class
in particular you intend to run. You only need to specify the module name.


```bash,no_run
java \
    --module-path ex.mod.jar \
    --module ex.mod
```

