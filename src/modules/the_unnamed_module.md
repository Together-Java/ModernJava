# The Unnamed Module

All packages that are not in a named module are placed in "the unnamed module."
This includes all the code you have written thus far and all code written without
a `module-info.java` alongside it.

This is generally okay. Modules as an organizational tool are most useful for sharing
code across "maintenance boundaries." Explicitly 

The unnamed module is special in that code within it `requires` every other module
and therefore can see every exported package and every class within.
