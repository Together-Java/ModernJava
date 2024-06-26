# Standard Input

Programs are pretty boring if they just make a machine warm and do some math.

There are a lot of ways to make a program interactive, but the easiest is to read
from what is called "standard input."

This function will be added to Java in a future version, but until then
copy paste this at the very top of all the code in this section.

```java,no_run
import java.util.Scanner;

Scanner scanner = new Scanner(System.in);

String input(String message) {
    System.out.print(message);
    return scanner.nextLine();
}
```