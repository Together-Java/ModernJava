# Run Java Programs

If you've properly set up Java on your machine you should be able to use the `java` command
to run any code on your machine.

Just write `java` followed by the path to a file containing Java code.[^eventually]

Say we had this code in a file named `Main.java`

```java
void main() {
    System.out.println("Hello");
}
```

To run this, say `java Main.java`.

```bash
$ java Main.java
Hello
```

If the file is in a directory that is not your current working directory, you 
should include the full path.

```bash
$ java src/Main.java
Hello
```

[^eventually]: You can get away with just using your editor's run button for awhile, but this 
will eventually become important to know.