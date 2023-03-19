# Access Individual Elements

Given an array, you can access any of its elements by index. 

You write the name of a variable containing an array, `[`, a number, and then a `]`.

The first element can be accessed by using `0`, the second by using `1`, and so on.

```java
String[] lyrics = { "you", "say", "goodbye" };

String you = lyrics[0];
System.out.println(you);

int say = lyrics[1];
System.out.println(say);

int goodbye = lyrics[2];
System.out.println(goodbye);
```

The index of the element can also come from a variable.

```java
int index = 2;
String[] lyrics = { "I", "say", "hello" };

System.out.println(lyrics[index]);
```

If you give a number equal to or greater than the length of the array or a number less than zero,
you will get an error.

```java
String[] lyrics = { "I", "say", "hi" };
// Crash!
lyrics[999];
```

```java
String[] lyrics = { "you", "say", "low" };
// Crash!
lyrics[-1];
```