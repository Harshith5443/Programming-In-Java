````markdown
### Question 1

**Problem:**  
Write a Java program to check whether the given number is **Prime** or not.

**Input:** `7`

### Java Code

```java
public class P1 {
    public static void main(String[] args) {

        int num = 7;

        boolean prime = true;

        if (num <= 1) {

            prime = false;

        } else {

            for (int i = 2; i <= num / 2; i++) {

                if (num % i == 0) {

                    prime = false;
                    break;
                }
            }
        }

        if (prime) {

            System.out.println("Prime Number");

        } else {

            System.out.println("Not a Prime Number");
        }
    }
}
```
````
````markdown
### Question 2

**Problem:**  
Write a Java program to check whether the given number is **Prime** or not using a **method with parameter and return type**.

**Input:** `7`

### Java Code

```java
public class P2 {

    static boolean isPrime(int num) {

        if (num <= 1) {

            return false;
        }

        for (int i = 2; i <= num / 2; i++) {

            if (num % i == 0) {

                return false;
            }
        }

        return true;
    }

    public static void main(String[] args) {

        int num = 7;

        if (isPrime(num)) {

            System.out.println("Prime Number");

        } else {

            System.out.println("Not a Prime Number");
        }
    }
}
```

### Sample Output

```text
Prime Number
```
### Sample Output

```text
Prime Number
```
````
