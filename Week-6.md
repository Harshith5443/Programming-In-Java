````markdown id="q1palindromenumber"

### Question 1

**Problem:**  
Write a Java program to check whether the given number is a **Palindrome** or not.

**Input:** `121`

### Java Code

```java
public class P1 {
    public static void main(String[] args) {

        int num = 121;

        int temp = num;
        int rev = 0;

        while (num > 0) {

            int rem = num % 10;

            rev = rev * 10 + rem;

            num = num / 10;
        }

        if (temp == rev) {

            System.out.println("Palindrome");

        } else {

            System.out.println("Not a Palindrome");
        }
    }
}
```

### Sample Output

```text
Palindrome
```
````

````markdown
### Question 2

**Problem:**  
Write a Java program to find the **sum of digits of a number** using a **method with parameter and return type**.

**Input:** `12345`

### Java Code

```java
public class P2 {

    static int sum(int num) {

        int sum = 0;

        while (num > 0) {

            int rem = num % 10;

            sum += rem;

            num = num / 10;
        }

        return sum;
    }

    public static void main(String[] args) {

        int num = 12345;

        System.out.println("Sum of Digits : " + sum(num));
    }
}
```

### Sample Output

```text
Sum of Digits : 15
```
````
````markdown
### Question 3

**Problem:**  
Write a Java program to find the **sum of digits repeatedly until a single digit is obtained**.

**Input:** `948216083`

### Java Code

```java
public class P3 {

    static int sum(int num) {

        int sum = 0;

        while (num > 0) {

            int rem = num % 10;

            sum += rem;

            num = num / 10;
        }

        return sum;
    }

    public static void main(String[] args) {

        int num = 948216083;

        while (num > 9) {

            num = sum(num);
        }

        System.out.println("Single Digit : " + num);
    }
}
```

### Sample Output

```text
Single Digit : 5
```
````
````markdown
### Question 4

**Problem:**  
Write a Java program to find the **sum of the square of each digit repeatedly until a single digit is obtained**.

**Input:** `948216083`

### Java Code

```java
public class P4 {

    static int sumSquare(int num) {

        int sum = 0;

        while (num > 0) {

            int rem = num % 10;

            sum += rem * rem;

            num = num / 10;
        }

        return sum;
    }

    public static void main(String[] args) {

        int num = 948216083;

        while (num > 9) {

            num = sumSquare(num);
        }

        System.out.println("Single Digit : " + num);
    }
}
```

### Sample Output

```text
Single Digit : 4
```
````
````markdown
### Question 5

**Problem:**  
Write a Java program to find the **sum of the square of each digit repeatedly** until a single digit is obtained and check whether the result is **1 or 7**.

**Happy Number:**  
A number is called a **Happy Number** if repeatedly replacing the number by the sum of the squares of its digits eventually reaches **1**.

**Input:** `19`

### Java Code

```java
public class P5 {

    static int sumSquare(int num) {

        int sum = 0;

        while (num > 0) {

            int rem = num % 10;

            sum += rem * rem;

            num = num / 10;
        }

        return sum;
    }

    public static void main(String[] args) {

        int num = 19;

        while (num > 9) {

            num = sumSquare(num);
        }

        if (num == 1 || num == 7) {

            System.out.println("Happy Number");

        } else {

            System.out.println("Not a Happy Number");
        }
    }
}
```

### Sample Output

```text
Happy Number
```
````
````markdown
### Question 6

**Problem:**  
Write a Java program to find the **factorial of a number**.

**Input:** `5`

### Java Code

```java
public class P6 {
    public static void main(String[] args) {

        int num = 5;

        int fact = 1;

        for (int i = 1; i <= num; i++) {

            fact = fact * i;
        }

        System.out.println("Factorial of " + num + " : " + fact);
    }
}
```

### Sample Output

```text
Factorial of 5 : 120
```
````

````markdown
# Question 7

**Problem:**  
Write a Java program to check whether the given number is a **Strong Number** or not using a **method**.

**Input:** `145`

## Java Code

```java
public class P7 {

    static int factorial(int num) {

        int fact = 1;

        for (int i = 1; i <= num; i++) {

            fact = fact * i;
        }

        return fact;
    }

    public static void main(String[] args) {

        int num = 145;

        int temp = num;
        int sum = 0;

        while (num > 0) {

            int rem = num % 10;

            sum += factorial(rem);

            num = num / 10;
        }

        if (temp == sum) {

            System.out.println("Strong Number");

        } else {

            System.out.println("Not a Strong Number");
        }
    }
}

```
