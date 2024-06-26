# Declaration

To put a class into a package you need to do two things.

First, put a "package declaration" at the top of the file. This looks like the word `package` followed by the name of the package and a `;`

```java,no_run
package dungeon;

class BugBear {

}
```

Then you need to make sure that the `.java` file is in a folder matching the name of
that package.

So, for the example above, if your code was previously laid out like this

```
src/
   BugBear.java
```

It needs to be changed to this.

```
src/
  dungeon/
    BugBear.java
```