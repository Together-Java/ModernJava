# Requires

Code within modules can only use classes defined in packages
that are part of its module or are in exported packages of modules it
"requires."

```java,no_run
module reality {
    exports earth;
    exports sea;
    exports sky;
}
```

```java
module human {
    // Code within this "human" module
    // will have access to classes in
    // the "earth," "sea," and "sky" packages.
    requires reality;
}
```

Modules can both require other modules and
export packages for other modules to use.

```java
module human {
    requires reality;

    exports sadness;
}
```

These `requires` are not allowed to form "cycles."
This means that `cat` cannot require `dog` if `dog` also
requires `cat`, indirectly or otherwise.

```java,no_run
module dog {
    requires cat;
}
```

```java,no_run
// Apologies to any hit Nickelodeon shows
// but this is unacceptable.
module cat {
    requires dog;
}
```