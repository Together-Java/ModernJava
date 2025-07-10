# Challenges


Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt


## Challenge 1.

Will this code run? Why or why not.

```java
int compute(int x) {
    if (x == 0) {
        return null;
    }
    else {
        return x * x;
    }
}

void main() {
    System.out.println(compute(5));
}
```

## Challenge 2.

Write a method which takes in an `Integer[]` representing
a series of distances and prints out every distance
followed by ` kilometers`.

So if the array has `1`, `2`, and `3` you should output

```
1 kilometers
2 kilometers
3 kilometers
```

If this method is given `null`, it should act as if it
was given an empty array.


```java,editable
void printDistances(Integer[] distances) {

}

void main() {
    printDistances(new Integer[] {
        45,
        99,
        23
    });
}
```

## Challenge 3.

Write a method called `onlyPositive` which takes in an `int` and returns
the same value out if the number is greater than zero.

If the number is less than or equal to zero, return `null`.

```java,editable
// Write onlyPositive here

void main() {
    // 45
    System.out.println(
        onlyPositive(45)
    );

    // 46
    System.out.println(
        onlyPositive(45) + 1
    );

    // null
    System.out.println(
        onlyPositive(0)
    );

    // null
    System.out.println(
        onlyPositive(-1)
    );
}
```

## Challenge 4.

Will the following code work? Why or why not?

```java
void main() {
    int ducks = 5;
    Integer sparrows = 3;

    int birds = ducks + sparrows;

    System.out.println(birds);
}
```

## Challenge 4.

Will the following code work? Why or why not?

```java
void main() {
    char[] face = new char[] { ':', ')' };
    Character[] smile = face;

    System.out.println(smile);
}
```

## Challenge 5.

Will the following code work? Why or why not?

```java
void main() {
    char[] face = new char[] { ':', ')' };

    Character[] smile = new Character[face.length];
    for (int i = 0; i < face.length; i++) {
        smile[i] = face[i];
    }
    
    System.out.println(smile);
}
```