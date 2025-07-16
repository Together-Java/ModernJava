# Information Hiding

When encapsulating, your fundamental activity is finding
ways to hide information that you consider to be 
implementation details.

If you did not hide this information and
you have a large number of consumers[^if], you would never
be able to change those implementation details. Your consumers
can be coupled to them.

Something to be careful of with respect to this is "side channels."
If you use the mechanisms Java gives you to hide a field from people
you can get pretty far, but you still need to be wary of accidentally allowing
people to do things you don't want.

```java,no_run
import java.util.ArrayList;

class Total {
    private final ArrayList<Integer> nums;

    Total() {
        this.nums = new ArrayList<>();
    }

    void add(int num) {
        nums.add(num);
    }

    int total() {
        int sum = 0;
        for (int num : nums) {
            sum += num;
        }
        return sum;
    }

    @Override
    public String toString() {
        return "Total[" + nums + "]";
    }
}
```

In the code above the `Total` class hides a field holding an `ArrayList`
and just exposes the total of the numbers added to it.

```java,no_run
void main() {
    var total = new Total();
    total.add(3);
    total.add(2);
    total.add(1);

    IO.println(total.total());
}
```

This lets it later on decide to maybe not store the list of numbers at all and instead keep a running total.

```java,no_run
import java.util.ArrayList;

class Total {
    private int runningTotal;

    Total() {
        this.runningTotal = 0;
    }

    void add(int num) {
        runningTotal += num;
    }

    int total() {
        return runningTotal;
    }

    @Override
    public String toString() {
        return "Total[" + runningTotal + "]";
    }
}
```

The problem is that if you had called `.toString()` on the previous implementation
you might have gotten a `String` that looks like `Total[[3, 2, 1]]`. The information
of what numbers are in the list was exposed there.

With enough people using this code some motivated moron will work backwards
from that `String` representation to get at the underlying list. Now if you changed the implementation
you would break their code.

We would call that a "side channel." The information is exposed, just through an API you didn't consider.
How you handle that is heavily dependent on the exact situation, but its a category of issue you should know about.


[^if]: Again, if. These concerns do not apply as much to 
programs written at smaller scales or programs written
_within_ some encapsulation boundary. Don't get too paranoid
about needing to hide things.