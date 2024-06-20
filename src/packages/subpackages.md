# Subpackages

Packages can also have subpackages.

What this looks like is for any package with a `.` in its name - say `my.fun.project` -
you need a new folder.

So if you have a class like this

```java
package my.fun.project;

public class Apple {}
```

It should be in a folder structure like this

```
src/
  my/
    fun/
      project/
        Apple.java
```

And the fully qualified class name would be `my.fun.project.Apple`.