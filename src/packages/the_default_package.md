# The Default Package

When your classes don't have a package declaration, we say those are in the "default package."

```java,no_run
// No package declaration means default package
public class Elf {

}
```

Classes in the default package cannot be imported by classes
in named packages, regardless of if those classes are public.

```java,no_run
package villager;

public class Villager {
    // No way to reference Elf directly,
    // even if Elf is public
}
```

Because of this restriction[^andmore] you will mostly use the default package
when you are feeling lazy or are making a smaller program.

[^andmore]: And more to come!