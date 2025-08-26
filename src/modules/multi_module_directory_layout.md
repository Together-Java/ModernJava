# Multi-Module Directory Layout

If you yourself want to develop a project using multiple of your own modules
there is a special way to layout the files to do so.

First, make folders with the name of each module. If a module name
has a `.` in it the folder should too.

```text,no_run
reality/
backrooms/
horrible.monsters/
```

Then in those folders under a `src` folder put the `module-info.java` files.[^src]

```text,no_run
reality/
  src/
    module-info.java
backrooms/
  src/
    module-info.java
horrible.monsters/
  src/
    module-info.java
```

From there you can put all the classes you want into each module, so long as they don't conflict
or create split packages.

```text,no_run
reality/
  src/
    earth/
      Dirt.java
      Worm.java
    sea/
      Starfish.java
    sky/
      Cloud.java
    module-info.java
backrooms/
  src/
    backrooms/
      YellowCarpet.java
    module-info.java
horrible.monsters/
  src/
    horrible/
      monsters/
        Slime.java
        Skeleton.java
    module-info.java
```

This can be helpful in structuring larger projects.

[^src]: The `src` folder isn't technically required. You will see what a `--module-source-path` looks like in a bit. I think its a good idea anyways.