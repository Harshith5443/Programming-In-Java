````markdown id="l4n8qm"
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
### Sample Output

```text
Enter a number: 25
Positive
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



### Question 3

**Problem:**  
Write a Java program to find the **largest of two numbers**.

String result=max>min? "Even":"Odd";
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


### Question 4

**Problem:**  
Write a Java program to find the **largest of three numbers**.

### Java Code

```java
import java.util.Scanner;

public class P4 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the first number: ");
        int num1 = sc.nextInt();

        System.out.print("Enter the second number: ");
        int num2 = sc.nextInt();

        System.out.print("Enter the third number: ");
        int num3 = sc.nextInt();

        if (num1 >= num2 && num1 >= num3) {
            System.out.println("Largest number: " + num1);
        } else if (num2 >= num1 && num2 >= num3) {
            System.out.println("Largest number: " + num2);
        } else {
            System.out.println("Largest number: " + num3);
        }

        sc.close();
    }
}
```

### Sample Output

```text
Enter the first number: 25
Enter the second number: 18
Enter the third number: 32
Largest number: 32
```

````markdown id="v5m2qd"
### Question 5

**Problem:**  
Write a Java program to check whether a given year is a **Leap Year** or **Not a Leap Year**.

### Java Code

```java
import java.util.Scanner;

public class P5 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a year: ");
        int year = sc.nextInt();

        if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
            System.out.println(year + " is a Leap Year.");
        } else {
            System.out.println(year + " is Not a Leap Year.");
        }

        sc.close();
    }
}
```

### Sample Output

```text
Enter a year: 2024
2024 is a Leap Year.
```
````

````


### Sample Output

```text
Enter the first number: 25
Enter the second number: 18
Largest number: 25
```

````markdown
### Question 6

**Problem:**  
Write a Java program to check whether a given character is a **Vowel** or **Consonant**.

### Java Code

```java
import java.util.Scanner;

public class P6 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a character: ");
        char ch = sc.next().charAt(0);

        if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' ||
            ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U') {
            System.out.println(ch + " is a Vowel.");
        } else {
            System.out.println(ch + " is a Consonant.");
        }

        sc.close();
    }
}
```

### Sample Output

```text
Enter a character: A
A is a Vowel.
```
````
````markdown id="q7up2l"
### Question 7

**Problem:**  
Write a Java program to check whether a given character is **Uppercase** or **Lowercase**.

### Java Code

```java
import java.util.Scanner;

public class P7 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a character: ");
        char ch = sc.next().charAt(0);

        if (ch >= 'A' && ch <= 'Z') {
            System.out.println(ch + " is an Uppercase letter.");
        } else if (ch >= 'a' && ch <= 'z') {
            System.out.println(ch + " is a Lowercase letter.");
        } else {
            System.out.println("Invalid input. Please enter an alphabet.");
        }

        sc.close();
    }
}
```

### Sample Output

```text
Enter a character: G
G is an Uppercase letter.
```
````
````markdown id="v8elgv"
### Question 8

**Problem:**  
Write a Java program to check whether a person is **eligible to vote** based on their age.

### Java Code

```java
import java.util.Scanner;

public class P8 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your age: ");
        int age = sc.nextInt();

        if (age >= 18) {
            System.out.println("You are eligible to vote.");
        } else {
            System.out.println("You are not eligible to vote.");
        }

        sc.close();
    }
}
```

### Sample Output

```text
Enter your age: 20
You are eligible to vote.
```
````
````markdown id="z9pass"
### Question 9

**Problem:**  
Write a Java program to check whether a student has **passed** or **failed** based on their marks.

### Java Code

```java
import java.util.Scanner;

public class P9 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the marks: ");
        int marks = sc.nextInt();

        if (marks >= 35) {
            System.out.println("Student has Passed.");
        } else {
            System.out.println("Student has Failed.");
        }

        sc.close();
    }
}
```

### Sample Output

```text
Enter the marks: 78
Student has Passed.
```
````
````markdown id="g10mark"
### Question 10

**Problem:**  
Write a Java program to **calculate the grade** based on the student's marks.

| Marks | Grade |
|--------|-------|
| 90–100 | A |
| 80–89 | B |
| 70–79 | C |
| 60–69 | D |
| Below 60 | F |

### Java Code

```java
import java.util.Scanner;

public class P10 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the marks: ");
        int marks = sc.nextInt();

        if (marks >= 90 && marks <= 100) {
            System.out.println("Grade: A");
        } else if (marks >= 80) {
            System.out.println("Grade: B");
        } else if (marks >= 70) {
            System.out.println("Grade: C");
        } else if (marks >= 60) {
            System.out.println("Grade: D");
        } else if (marks >= 0) {
            System.out.println("Grade: F");
        } else {
            System.out.println("Invalid marks.");
        }

        sc.close();
    }
}
```

### Sample Output

```text
Enter the marks: 85
Grade: B
```
````


