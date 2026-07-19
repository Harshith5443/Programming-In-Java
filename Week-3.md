````markdown id="q1rev"

### Question 1

**Problem:**  
Write a Java program to **reverse a given string**.

**Input:** `java`

### Java Code

```java
public class P1 {
    public static void main(String[] args) {

        String str = "java";
        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev = rev + str.charAt(i);
        }

        System.out.println("Original String: " + str);
        System.out.println("Reversed String: " + rev);
    }
}
```

### Sample Output

```text
Original String: java
Reversed String: avaj
```
````

````markdown id="q1pal"

### Question 1

**Problem:**  
Write a Java program to check whether the given string is a **Palindrome**.

**Input:** `java`

### Java Code

```java
public class P1 {
    public static void main(String[] args) {

        String str = "java";
        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev = rev + str.charAt(i);
        }

        if (str.equals(rev)) {
            System.out.println(str + " is a Palindrome.");
        } else {
            System.out.println(str + " is Not a Palindrome.");
        }
    }
}
```

### Sample Output

```text
java is Not a Palindrome.
```
````

