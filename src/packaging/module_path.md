# --module-path

After packaging code into a JAR file you can put that
JAR onto the `--module-path` in the same way you would a folder
of classes.

```bash
java \
    --module-path ex.mod.jar \
    --add-modules ALL-MODULE-PATH
    some.pkg.Main
```

If you have multiple JARs to put on the module path
you can do so by separating them with a `:`.[^windows]

```bash
java \
    --module-path ex.mod.jar:other.thing.jar \
    --add-modules ALL-MODULE-PATH
    some.pkg.Main
```

Instead of `--add-modules ALL-MODULE-PATH` followed by a class name you
can use `--module` followed by `<module name>/<class name>`

```bash,no_run
java \
    --module-path ex.mod.jar \
    --module ex.mod/some.pkg.Main
```

[^windows]: On Windows instead of a `:` you use a `;`. I am assuming when making these examples
that you are using Windows Subsystem for Linux. If you are not, just adjust as needed.