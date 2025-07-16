# Semicolons

The `;` at the end of each of those lines is a "semicolon".

```java
~void main(){
IO.print("Hello, "); // <-- this thing
                       //  ^
~}
```

It indicates that the statement has finished. A "statement" is a line of code that "does something."
The reason we call it a statement and not just a "line of code" is that it can technically span multiple lines and be
more complicated than these examples.

```java
~void main(){
IO.print(
    "Hello, "
);
~}
```

The `;` at the end is needed so that Java knows that the statement is over.
You need to put a `;`
at the end of every statement. If you do not, Java will get confused and your code will not work.

If you happen to have an extra semi-colon or two that is technically okay. It just reads it as an "empty statement." It's pointless, but it is allowed.

```java
~void main() {
IO.print(
    "Hello, "
);;
~}
```

Or even

```java
~void main() {
IO.print(
    "Hello, "
);

  // Technically legal, but kinda sus

  ;;;;;;;;;;;;;
  ;;;        ;;
  ;;;        ;;
  ;;;;;;;;;;;;;
  ;;   ;;;   ;;
  ;;;;;;;;;;;;;
  ; ;       ; ;
  ; ;       ; ;
  ;;;       ;;;
~}
```
