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

````markdown id="q2reverseeachwordlength"

### Question 2

**Problem:**  
Write a Java program to **reverse each word whose length is greater than 2** in the given string.

**Input:** `iS method is a Block of Statement in Java`

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

        String str = "iS method is a Block of Statement in Java";

        String[] s1 = str.split(" ");

        for (int i = 0; i < s1.length; i++) {

            if (s1[i].length() > 2) {

                System.out.print(rev(s1[i]) + " ");
            }
        }
    }
}
```

### Sample Output

```text
dohtem kcolB tnemetatS avaJ
```
````
````markdown id="q3findpalindromewords"

### Question 3

**Problem:**  
Write a Java program to **print only the palindrome words** from the given string.

**Input:**  
`mom knows Malayalam.she is from katak place which is in Gadag distirct`

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

        String str = "mom knows Malayalam she is from katak place which is in Gadag distirct";

        String[] s1 = str.split(" ");

        for (int i = 0; i < s1.length; i++) {

            String st = rev(s1[i]);

            if (s1[i].equalsIgnoreCase(st)) {

                System.out.print(s1[i] + " ");
            }
        }
    }
}
```

### Sample Output

```text
mom Malayalam katak Gadag
```
````
````markdown id="q3substring"

### Question 3

**Problem:**  
Write a Java program to demonstrate the **`substring()`** method.

**Input:** `MethodOverloading`

### Syntax

```java
// Returns the substring from the given begin index to the end of the string
String substring(int beginIndex)

// Returns the substring from the given begin index to the given end index
String substring(int beginIndex, int endIndex)
```

> **Note:** `beginIndex` is inclusive and `endIndex` is exclusive.

### Java Code

```java
public class P3 {
    public static void main(String[] args) {

        String str = "MethodOverloading";

        System.out.println(str.substring(0, 6));
        System.out.println(str.substring(6));
        System.out.println(str.substring(6, 10));
        System.out.println(str.substring(10));
    }
}
```

### Sample Output

```text
Method
Overloading
Over
loading
```
````


