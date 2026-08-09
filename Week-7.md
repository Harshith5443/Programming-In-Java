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
```text
Prime Number
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

````
````markdown
### Question 3

**Problem:**  
Write a Java program to **print the next prime number** after the given number.

**Input:** `7`

### Java Code

```java
public class P3 {

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

        int next = num + 1;

        while (!isPrime(next)) {

            next++;
        }

        System.out.println("Next Prime Number : " + next);
    }
}
```

### Sample Output

```text
Next Prime Number : 11
```

````
````markdown
### Question 4

**Problem:**  
Write a Java program to **print all Prime Numbers in a given range**.

**Input:** `10 to 30`

### Java Code

```java
public class P4 {

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

        int start = 10;
        int end = 30;

        for (int i = start; i <= end; i++) {

            if (isPrime(i)) {

                System.out.println(i);
            }
        }
    }
}
```

### Sample Output

```text
11
13
17
19
23
29
```

````
````markdown
### Question 5

**Problem:**  
Write a Java program to check whether the given number is **Prime or Not using count**.

**Input:** `7`

### Java Code

```java
public class P5 {

    public static void main(String[] args) {

        int num = 7;

        int count = 0;

        for (int i = 1; i <= num; i++) {

            if (num % i == 0) {

                count++;
            }
        }

        if (count == 2) {

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
