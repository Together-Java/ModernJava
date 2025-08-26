# jar

The tool you use to package up class files in Java is called `jar`.
The output from this tool is a "JAR file."

To make a JAR file, first compile your code into a folder.

If you do this by listing all the files out one-by-one, your output
folder will be structured something like the following.

```text,no_run
output/
  some_pkg/
    A.class
    nested/
      B.class
```

If you did it using the `--module-source-path` your class files will be nested
under a folder with the name of the module.

```text,no_run
output/
  ex.mod/
    module-info.class
    some_pkg/
      A.class
      nested/
        B.class
```

Then use a command like the following:

```bash,no_run
jar \
    --create \
    --file ex.mod.jar \
    -C output/ex.mod .
```

The `--create` part means "we are creating a new jar file"
and `--file` says what file to put the jar in. For the file name
you should generally use the name of the module followed by `.jar`.[^mods]
This is technically optional though.

The `-C` flag is where it gets interesting. The `jar` tool works somewhat like how your terminal
does when you `cd` into directories.

The tool starts at the directory you are running it at.

```text,no_run
project/ <--- jar "is here"
  output/
    ex.mod/
      module-info.class
     some_pkg/
        A.class
        nested/
          B.class
```

Then with `-C` you "**C**hange" into a directory.

```text,no_run
project/ 
  output/
    ex.mod/ <--- jar is here after "-C output/ex.mod"
      module-info.class
     some_pkg/
        A.class
        nested/
          B.class
```

After that you are meant to specify what files you want to add into the jar. Just putting one period (`.`)
means "take everything in this folder." Hence `-C output/ex.mod .` puts all those files into the final JAR.

[^mods]: And, like I've mentioned before, you should ideally be packaging up code
in modules.