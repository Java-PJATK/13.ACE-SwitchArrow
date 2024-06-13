# 13.ACE-SwitchArrow  
  
Starting from Java 14, instead of the colon, one can use the "arrow", represented by the two-character '->' symbol (note that mixing colons and arrows in one switch statement is not allowed). With this syntax:
- The "fall through" feature is turned off.
- To the right of the arrow, you can use:
  1. Single statement or expression,
  2. A block enclosed in braces,
  3. A throw statement.

For example, in the following code snippet, no break statements are used:

## Listing 13 ACE-SwitchArrow/SwitchArrow.java Page 34  

```java
import java.util.Scanner;

public class SwitchArrow {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.print("Enter a natural number -> ");
        int k = scan.nextInt();
        scan.close();

        String part1 = k + " is of the form ";
        String part2 = null;

        switch (k % 4) {
            case 0 -> part2 = "4n";
            case 1 -> part2 = "4n+1";
            case 2 -> part2 = "4n+2";
            case 3 -> part2 = "4n+3";
            default -> {
                part2 = " ... probably negative";
                System.out.println("You were expected to enter a *natural* number!");
            }
        }

        System.out.println(part1 + part2);
    }
}
```
