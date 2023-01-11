# Formatting


You may have noticed that after each `{` all the code that comes after it is "indented" in one "level."

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

Then, when there is a `}` everything is "de-dented" one level.

I will kindly ask that you try to stick to this rule when writing your own code as well.
If you try to find help online and you haven't, it will be dyslexically hard for people
to read your code.

So don't do this.

```java
public class Main {
public static void main(String[] args) {
System.out.println("Hello, World!");
}}
```

Don't do this.

```java
public class Main 
    {
    public static void main(String[] args) 
            {
        System.out.println("Hello, World!");
            }
    }
```

Don't do this.

```java
public class Main {
    public static void main(String[] args) 
            {    System.out.println("Hello, World!");
    }}
```

And this is just insane.

```java
public class Main { public static void main(String[] args) { System.out.println("Hello, World!"); } }
```

Do this.

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

And keep in mind that this rule of thumb applies to every language constrict that requires a `{` and `}` many of which I will introduce later.
