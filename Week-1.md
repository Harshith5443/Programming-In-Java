# Question 1

**Problem:**  
Write a Java program to check whether a given number is Positive, Negative, or Zero.

## Java Code

```java
import java.util.Scanner;

public class P1 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int n = sc.nextInt();

        if (n > 0) {
            System.out.println("Positive");
        } else if (n < 0) {
            System.out.println("Negative");
        } else {
            System.out.println("Zero");
        }

        sc.close();
    }
}
```

## Sample Output

```text
Enter a number: 25
Positive
```
