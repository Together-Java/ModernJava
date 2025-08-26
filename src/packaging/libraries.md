# Libraries

It is often the case that it isn't practical to produce a program
using only the modules that come with Java. 

To cope with this reality you can use code written by others
as "libraries" of functionality.[^procuring]

When running a Java program from source you can provide the libraries
using `--module-path <path to library jar> --add-modules ALL-MODULE-PATH`.
So if you had a library named `tangerine.jar` you could run something like the following
command.

```bash,no_run
java \
    --module-path tangerine.jar \
    --add-modules ALL-MODULE-PATH \
    src/Main.java
```

You do not need the `--add-modules ALL-MODULE-PATH` if your code is itself inside of a named
module. The `requires` in the module take care of telling Java what to include.

```bash,no_run
java \
    --module-path tangerine.jar \
    ex.mod/src/Main.java
```

If you use libraries you need to provide the same flags to `javac` when compiling
your own code to share.

```bash,no_run
java \
    -g \
    -d output \
    --module-path tangerine.jar \
    --module-source-path "./*/src" \
    --module example.module
```

Now that you can package your own code into JARs you can share code with others
for this purpose.

[^procuring]: Libraries can depend on libraries which depend on other libraries in sprawling nightmare graphs. For now let us assume that the libraries you want to use are relatively self-contained
and reasonable to download manually. Dependency resolution and procurement can be a topic for a later day.
