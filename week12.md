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
