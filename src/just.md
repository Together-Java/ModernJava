# just

As you might be noticing, commands in the terminal can get quite long.

Not only are you liable to make a mistake typing out `java --module-path a:bunch:of:files --add-modules ALL-MODULE-PATH src/Main.java` for the 20th time, you are also just going to get annoyed doing so.[^nature]

To remember what commands to run to do certain tasks I reccomend using a tool called "[just](https://github.com/casey/just)."

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

This section is ultimately optional, but you will quickly see a need for _something_
that helps you remember commands.

[^nature]: Generally when something is "your job" or "the right way" you do need to just suck it up
and do the manual labor. But there are limits to this, human nature being what it is.