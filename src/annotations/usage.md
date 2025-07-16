# Usage

Once you have defined an annotation you can use it to mark different elements
of your program.

```java,no_run
@interface Even {
}

@interface NumberWrapper {
}

@NumberWrapper // Here @NumberWrapper is annotating the EvenNumber class
class EvenNumber {
    final @Even int x; // And @Even is annotating the "x" field

    EvenNumber(int x) {
        if (x % 2 != 0) {
            throw new IllegalArgumentException(Integer.toString(x));
        }
        this.x = x;
    }
}
```

You can place an annotation on nearly any "structural" element of a program. 
This includes classes, method definitions, fields, and more.
