# The Unnamed Module

All packages that are not in a named module are placed in "the unnamed module."
This includes all the code you have written thus far and all code written without
a `module-info.java` alongside it.

The unnamed module is special in that code within it `requires` every other module
and therefore can see every exported package and every class within.

It is fine to have your code in the unnamed module, but code you get from other people
should generally be in named modules. This is because modules are mostly
useful for sharing code across "maintenance boundaries." 

If you are not going to be sharing your code with another person then
the ability to have "unexported packages" matters less. If you are
the person who code is shared with, the group sharing it with you
will expect you to not touch classes in packages they did not export.

