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

Note:String result=max>min? "Even":"Odd";
Math.max(a,b);

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
Enter a year: 2024
2024 is a Leap Year.
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
````
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
````
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
````
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
````
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
````
````markdown id="q11char"
### Question 11

**Problem:**  
Write a Java program to check whether a given character is an **Alphabet**, **Digit**, or **Special Character**.

### Java Code

```java
import java.util.Scanner;

public class P11 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a character: ");
        char ch = sc.next().charAt(0);

        if ((ch >= 'A' && ch <= 'Z') || (ch >= 'a' && ch <= 'z')) {
            System.out.println(ch + " is an Alphabet.");
        } else if (ch >= '0' && ch <= '9') {
            System.out.println(ch + " is a Digit.");
        } else {
            System.out.println(ch + " is a Special Character.");
        }

        sc.close();
    }
}
```

### Sample Output

```text
Enter a character: @
@ is a Special Character.
```
````
````markdown id="q12code"
### Question 12

**Problem:**  
Write a Java program to display the **department name** based on the given department code.

| Code | Department |
|------|------------|
| 101 | HR |
| 102 | Finance |
| 103 | IT |
| 104 | Sales |
| Others | Invalid Department Code |

### Java Code

```java
import java.util.Scanner;

public class P12 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the department code: ");
        int code = sc.nextInt();

        if (code == 101) {
            System.out.println("Department: HR");
        } else if (code == 102) {
            System.out.println("Department: Finance");
        } else if (code == 103) {
            System.out.println("Department: IT");
        } else if (code == 104) {
            System.out.println("Department: Sales");
        } else {
            System.out.println("Invalid Department Code");
        }

        sc.close();
    }
}
```

### Sample Output

```text
Enter the department code: 101
Department: HR
```
````
````markdown id="q16atm"
### Question 16

**Problem:**  
Write a Java program to display the following **ATM menu options**.

1. Balance
2. Deposit
3. Withdraw
4. Exit

### Java Code

```java
import java.util.Scanner;

public class P16 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.println("===== ATM Menu =====");
        System.out.println("1. Balance");
        System.out.println("2. Deposit");
        System.out.println("3. Withdraw");
        System.out.println("4. Exit");

        System.out.print("Enter your choice: ");
        int choice = sc.nextInt();

        if (choice == 1) {
            System.out.println("Balance Selected");
        } else if (choice == 2) {
            System.out.println("Deposit Selected");
        } else if (choice == 3) {
            System.out.println("Withdraw Selected");
        } else if (choice == 4) {
            System.out.println("Thank you for using the ATM.");
        } else {
            System.out.println("Invalid Choice");
        }

        sc.close();
    }
}
```

### Sample Output

```text
===== ATM Menu =====
1. Balance
2. Deposit
3. Withdraw
4. Exit
Enter your choice: 2
Deposit Selected
```
````
````markdown id="q17bill"
### Question 17

**Problem:**  
Write a Java program to implement a **Simple Restaurant Ordering System** and calculate the bill based on the selected item.

| Item | Price (₹) |
|------|----------:|
| 1. Pizza | 250 |
| 2. Burger | 150 |
| 3. Sandwich | 120 |
| 4. Coffee | 80 |

### Java Code

```java
import java.util.Scanner;

public class P17 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.println("===== Restaurant Menu =====");
        System.out.println("1. Pizza - ₹250");
        System.out.println("2. Burger - ₹150");
        System.out.println("3. Sandwich - ₹120");
        System.out.println("4. Coffee - ₹80");

        System.out.print("Enter your choice: ");
        int choice = sc.nextInt();

        if (choice == 1) {
            System.out.println("Item: Pizza");
            System.out.println("Bill Amount: ₹250");
        } else if (choice == 2) {
            System.out.println("Item: Burger");
            System.out.println("Bill Amount: ₹150");
        } else if (choice == 3) {
            System.out.println("Item: Sandwich");
            System.out.println("Bill Amount: ₹120");
        } else if (choice == 4) {
            System.out.println("Item: Coffee");
            System.out.println("Bill Amount: ₹80");
        } else {
            System.out.println("Invalid Choice");
        }

        sc.close();
    }
}
```

### Sample Output

```text
===== Restaurant Menu =====
1. Pizza - ₹250
2. Burger - ₹150
3. Sandwich - ₹120
4. Coffee - ₹80
Enter your choice: 2
Item: Burger
Bill Amount: ₹150
```
````

