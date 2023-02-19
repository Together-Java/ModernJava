# Equality

You can check if two `String`s have the same contents by using `.equals`.

```java
String lyricOne = "Green, Green, Dress";
String lyricTwo = "Green, Green, Dress";

boolean areSameLyric = lyricOne.equals(lyricTwo);
boolean isMyName = lyricOne.equals("Bop Bop");

System.out.println(areSameLyric);
System.out.println(isMyName);
```

You write one `String` on the left, `.equals`, and then the `String` you want to check it
against inside of parentheses.

To see if strings have different contents, you need to use the not operator (`!`) on
the result of `.equals`.

```java
String bow = "bow";
String wow = "WOW";

boolean areNotSame = !bow.equals(wow);

System.out.println(areNotSame);
```
