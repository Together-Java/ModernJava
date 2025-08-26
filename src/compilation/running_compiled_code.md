# Running Compiled Code

The way you ultimately run your compiled code depends on 
whether or not all your code is in packages.

If you have any classes in the unnamed package - which
will only be the case when said code is also not in a named
module - you should run your code like so:

```bash,no_run
java --class-path output Main
```

Where you can substitute `Main` for whatever the class you want to run is.
So if you want to run a class named `Impromptu` in the `chopin` package
you would run `java --class-path output chopin.Impromptu`.

`--class-path` should be self-explanatory. It is the path where `java`
will look for class files.

But if you do not have any classes in the unnamed package - which will
be hopefully be the case when you share code with others[^conflicts] -
you instead want to run your code like this.

```
java \
    --module-path output \
    --add-modules ALL-MODULE-PATH
    composers.Main
```

The `--module-path` option is very similar to the `--class-path` option. The difference
is that all the code on the `--module-path` will be loaded with more strict rules.[^before]

The `--add-modules ALL-MODULE-PATH` bit just means "load all the code on the module path."[^auth]

[^conflicts]: Remember the social convention of reverse domain name notation (`com.google`, etc)

[^before]: You can think of `--class-path` as sort of a "compatibility mode" for libraries 
and code written before Java had a concept of modules. The difference isn't super important
other than the very specific case of wanting to compile and run classes in the unnamed package.
Well that and "troublesome" libraries, but we will get to that later.

[^auth]: Chances are Java will make this the default in the future. For now you must write it though.