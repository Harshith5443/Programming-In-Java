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

