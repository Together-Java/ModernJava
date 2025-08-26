# Clean

If you compile code multiple times you should "clean"
your working directory before each compilation.

This is because when you run `javac -d output ...` the compiler
will simply dump class files into the destination folder.
It will not remove any "stale" class files from earlier compiler runs.

This can lead you to be in a state where you think your code is working
but if you ever compiled it again, from scratch, you would get errors.

The simplest way to handle this in bash is to use the `rm` tool. `rm` **r**e**m**oves
files. Before you run the compiler clear out any old output with `rm -rf output`.
`-rf` stands for "**r**ecursive" and "**f**orce." This is what you need to delete whole
folders.[^simple]

[^simple]: This technique - just deleting folders and doing the work from scratch again - can be slow.
The upside of this approach is that it is simple to understand.
It also probably doesn't matter since your computer is fast. When you need to really efficiently compile
huge codebases you turn to a special kind of program called a build tool. These are complex beasts but can
avoid unneccesary work.