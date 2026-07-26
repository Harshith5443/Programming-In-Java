````markdown id="q1reverseeachwordmethod"

### Question 1

**Problem:**  
Write a Java program to **reverse each word** in the given string using a **separate reverse method**.

**Input:** `java is programming language`

### Java Code

```java
public class Each {

    static String rev(String str) {

        char[] ch = str.toCharArray();

        int i = 0;
        int j = ch.length - 1;

        while (i < j) {

            char temp = ch[i];
            ch[i] = ch[j];
            ch[j] = temp;

            i++;
            j--;
        }

        return new String(ch);
    }

    public static void main(String[] args) {

        String str = "java is programming language";

        String[] s1 = str.split(" ");

        for (int i = 0; i < s1.length; i++) {

            System.out.print(rev(s1[i]) + " ");
        }
    }
}
```

### Sample Output

```text
avaj si gnimmargorp egaugnal
```
````

