````markdown
### Question 1

**Problem:**  
Write a Java program to print **"Hello Java" without using a semicolon**.

### Java Code

```java
public class P1 {
    public static void main(String[] args) {

        if (System.out.printf("Hello Java") == null) {
        }

        // Another way to write the program
        for (int i = 0; i < 1; System.out.println("Hello Java")) {
            i++;
        }
    }
}
```

### Sample Output

```text
Hello Java
Hello Java
```
````

````markdown
### Question 2

**Problem:**  
Write a Java program to **remove white spaces from a given sentence**.

### Java Code

```java
import java.util.Scanner;

public class P2 {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a sentence: ");
        String sentence = sc.nextLine();

        String result = sentence.replace(" ", "");

        System.out.println("Sentence without white spaces: " + result);

        sc.close();
    }
}
```

### Sample Output

```text
Enter a sentence: Hello Java Programming
Sentence without white spaces: HelloJavaProgramming
```
````



