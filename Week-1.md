````markdown
### Question 1

**Problem:**  
Write a Java program to check whether a given number is Positive, Negative, or Zero.

### Java Code

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



### Question 2

**Problem:**  
Write a Java program to check whether a given number is **Even or Odd**.

### Java Code

```java
import java.util.Scanner;

public class P2 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int n = sc.nextInt();

        if (n % 2 == 0) {
            System.out.println("Even");
        } else {
            System.out.println("Odd");
        }

        sc.close();
    }
}
```

### Sample Output

```text
Enter a number: 12
Even
```


### Sample Output

```text
Enter a number: 25
Positive
```




````
````markdown
### Question 3

**Problem:**  
Write a Java program to find the **largest of two numbers**.

### Java Code

```java
import java.util.Scanner;

public class P3 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the first number: ");
        int num1 = sc.nextInt();

        System.out.print("Enter the second number: ");
        int num2 = sc.nextInt();

        if (num1 > num2) {
            System.out.println("Largest number: " + num1);
        } else if (num2 > num1) {
            System.out.println("Largest number: " + num2);
        } else {
            System.out.println("Both numbers are equal.");
        }

        sc.close();
    }
}
```

### Sample Output

```text
Enter the first number: 25
Enter the second number: 18
Largest number: 25
```
````
