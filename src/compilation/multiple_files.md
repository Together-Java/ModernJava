# Compile Multiple Files

To have `javac` compile multiple files you have a few options.

The first is to simply list every file you want to compile one after
the other when calling `javac`.

```bash
javac -d output src/Main.java src/Other.java src/Another.java
```

This has the obvious downside of needing you to add new files to what can
become a large list over time.

If you get far enough in learning bash you can paper over this
with commonly available tools like `find`.

```bash
javac -d output $(find ./src -name "*.java" -type f)
```

Where the `$()` is bash syntax that runs the command in the parentheses and uses its
output as arguments to the command being run. `find` is a tool that lists all files that
match some criteria. In this case all files (as opposed to folders) that have a name that
ends with `.java`.

The other option is to structure your project using the multi-module directory layout.

```
your.project/
  src/
    code/
      Main.java
      Other.java
    module-info.java
```

If you do this then you can compile all the code in a module by using the `--module-source-path` and `--module` options.

```bash
javac -d output --module-source-path "./*/src" --module your.project
```

