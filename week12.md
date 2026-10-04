````markdown
# Pattern 1

## Question 1

**Problem:**  
Write a Java program to print the following pattern.

### Pattern

```text
* * *
* * *
* * *
```

### Java Code

```java
public class P1 {
    public static void main(String[] args) {

        for (int i = 1; i <= 3; i++) {
            for (int j = 1; j <= 3; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

### Sample Output

```text
* * *
* * *
* * *
```

````
````markdown
# Pattern 2

## Question 2

**Problem:**  
Write a Java program to print the following pattern.

### Pattern

```text
*
* *
* * *
* * * *
```

### Java Code

```java
public class P2 {
    public static void main(String[] args) {

        for (int i = 1; i <= 4; i++) {
            for (int j = 1; j <= 4; j++) {
                if (j <= i)
                    System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

### Sample Output

```text
*
* *
* * *
* * * *
```

````
````markdown
# Pattern 3

## Question 3

**Problem:**  
Write a Java program to print the following pattern.

### Pattern

```text
* * * * *
  * * * *
    * * *
      * *
        *
```

### Java Code

```java
public class P3 {
    public static void main(String[] args) {

        for (int i = 1; i <= 5; i++) {

            for (int j = 1; j <= 5; j++) {
                if (j >= i)
                    System.out.print("* ");
                else
                    System.out.print("  ");
            }

            System.out.println();
        }
    }
}
```

### Sample Output

```text
* * * * *
  * * * *
    * * *
      * *
        *
```

````
````markdown
# Pattern 4

## Question 4

**Problem:**  
Write a Java program to print the following pattern.

### Pattern

```text
* * * * *
 * * * *
  * * *
   * *
    *
```

### Java Code

```java
public class P4 {
    public static void main(String[] args) {

        for (int i = 1; i <= 5; i++) {

            for (int j = 1; j <= 5; j++) {
                if (j >= i)
                    System.out.print("* "); //Provide Space
                else
                    System.out.print(" ");
            }

            System.out.println();
        }
    }
}
```

### Sample Output

```text
* * * * *
 * * * *
  * * *
   * *
    *
```

````
````markdown
# Pattern 5

## Question 5

**Problem:**  
Write a Java program to print the following pattern.

### Pattern

```text
        *
      * *
    * * *
  * * * *
* * * * *
```

### Java Code

```java
public class P5 {
    public static void main(String[] args) {

        for (int i = 1; i <= 5; i++) {

            for (int j = 5; j >= 1; j--) {
                if (j <= i)
                    System.out.print("* ");
                else
                    System.out.print("  ");
            }

            System.out.println();
        }
    }
}
```

### Sample Output

```text
        *
      * *
    * * *
  * * * *
* * * * *
```

````
````markdown
# Pattern 6

## Question 6

**Problem:**  
Write a Java program to print the following pattern.

### Pattern

```text
* * * * *
*       *
*       *
*       *
* * * * *
```

### Java Code

```java
public class P6 {
    public static void main(String[] args) {

        for (int i = 1; i <= 5; i++) {

            for (int j = 1; j <= 5; j++) {

                if (i == 1 || i == 5 || j == 1 || j == 5)
                    System.out.print("* ");
                else
                    System.out.print("  ");
            }

            System.out.println();
        }
    }
}
```

### Sample Output

```text
* * * * *
*       *
*       *
*       *
* * * * *
```

````
````markdown
# Pattern 7

## Question 7

**Problem:**  
Write a Java program to print the following pattern.

### Pattern

```text
1
2 2
3 3 3
```

### Java Code

```java
public class P7 {
    public static void main(String[] args) {

        for (int i = 1; i <= 3; i++) {

            for (int j = 1; j <= i; j++) {
                System.out.print(i + " ");
            }

            System.out.println();
        }
    }
}
```

### Sample Output

```text
1
2 2
3 3 3
```

````
````markdown
# Pattern 8

## Question 8

**Problem:**  
Write a Java program to print the following pattern.

### Pattern

```text
1
2 3
4 5 6
7 8 9 10
```

### Java Code

```java
public class P8 {
    public static void main(String[] args) {

        int num = 1;

        for (int i = 1; i <= 4; i++) {

            for (int j = 1; j <= i; j++) {
                System.out.print(num + " ");
                num++;
            }

            System.out.println();
        }
    }
}
```

### Sample Output

```text
1
2 3
4 5 6
7 8 9 10
```

````
````markdown
# Pattern 9

## Question 9

**Problem:**  
Write a Java program to take a character as input and print the following pattern.

### Input

```text
A
```

### Pattern

```text
A
A A
A A A
A A A A
A A A A A
```

### Java Code

```java
import java.util.Scanner;

public class P9 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        char c = sc.next().charAt(0);

        for (int i = 1; i <= 5; i++) {

            for (int j = 1; j <= i; j++) {
                System.out.print(c + " ");
            }

            System.out.println();
        }
    }
}
```

### Sample Output

```text
A
A A
A A A
A A A A
A A A A A
```
