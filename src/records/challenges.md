# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Replace the usage of a normal class in the following code with a record.

```java,editable
import java.util.Arrays;

class InventoryItem {
    String name;

    InventoryItem(String name) {
        this.name = name;
    }
}

class Main {
    void main() {
        var item1 = new InventoryItem("sword");
        var item2 = new InventoryItem("shield");
        var item3 = new InventoryItem("armor");

        InventoryItem[] items = {
            item1,
            item2,
            item3
        };

        IO.println(Arrays.toString(items));
    }
}
```

## Challenge 2.

Make an instance of the `Tien` record and print it out.

```java,editable
enum TienMove {
    DODON_RAY,
    TRI_BEAM,
    EXPLODE
}

record Chiaotzu(
    Move memorableMove
) {}

record Tien(
    Chiaotzu onlyFriend,
    Move firstMove,
    Move secondMove
) {}

class Main {
    void main() {
        Tien tien;
        // CODE HERE
        IO.println(tien);
    }
}
```

## Challenge 3.

What will this program output when run? 

1. `true` then `true`
2. `true` then `false`
3. `false` then `true`
4. `false` then `false`

Write down your guess and then try running it.

```java
class Position {
    int x;
    int y;

    Position(int x, int y) {
        this.x = x;
        this.y = y;
    }
}

record Location(int x, int y) {}

class Main {
    void main() {
        var p1 = new Position(7, 1);
        var p2 = new Position(7, 1);
        IO.println(p1.equals(p2));

        var l1 = new Location(8, 3);
        var l2 = new Location(8, 3);
        IO.println(l1.equals(l2));
    }
}
```