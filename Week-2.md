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

````markdown
### Question 3

**Problem:**  
Write a Java program to replace **"Java" with "Python"** in the given string.

### Java Code

```java
public class P3 {
    public static void main(String[] args) {

        String str = "Java is Programming Language";

        String result = str.replace("Java", "Python");

        System.out.println("Original String: " + str);
        System.out.println("Modified String: " + result);
    }
}
```

### Sample Output

```text
Original String: Java is Programming Language
Modified String: Python is Programming Language
```
````

````markdown
### Given String

```java
String str = "MeThodOverLoAdiNG";
```

---

### Question 1

**Problem:**  
Write a Java program to print only **Uppercase Characters** from the given string.

### Java Code

```java
public class P1 {
    public static void main(String[] args) {

        String str = "MeThodOverLoAdiNG";

        System.out.println(str.replaceAll("[a-z]", ""));
    }
}
```

### Sample Output

```text
MTOLANG
```

---

### Question 2

**Problem:**  
Write a Java program to print only **Lowercase Characters** from the given string.

### Java Code

```java
public class P2 {
    public static void main(String[] args) {

        String str = "MeThodOverLoAdiNG";

        System.out.println(str.replaceAll("[A-Z]", ""));
    }
}
```

### Sample Output

```text
ehodverodi
```

---

### Question 3

**Problem:**  
Write a Java program to print only **Vowel Characters** from the given string.

### Java Code

```java
public class P3 {
    public static void main(String[] args) {

        String str = "MeThodOverLoAdiNG";

        System.out.println(str.replaceAll("[^aeiouAEIOU]", ""));
    }
}
```

### Sample Output

```text
eoOeoi
```

---

### Question 4

**Problem:**  
Write a Java program to print the **number of characters** in the given string.

### Java Code

```java
public class P4 {
    public static void main(String[] args) {

        String str = "MeThodOverLoAdiNG";

        System.out.println("Number of Characters: " + str.length());
    }
}
```

### Sample Output

```text
Number of Characters: 17
```

---

### Question 5

**Problem:**  
Write a Java program to print the **number of Vowels** in the given string.

### Java Code

```java
public class P5 {
    public static void main(String[] args) {

        String str = "MeThodOverLoAdiNG";

        System.out.println("Number of Vowels: "
                + str.replaceAll("[^aeiouAEIOU]", "").length());
    }
}
```

### Sample Output

```text
Number of Vowels: 6
```

---

### Question 6

**Problem:**  
Write a Java program to print the **number of Uppercase Characters** in the given string.

### Java Code

```java
public class P6 {
    public static void main(String[] args) {

        String str = "MeThodOverLoAdiNG";

        System.out.println("Number of Uppercase Characters: "
                + str.replaceAll("[a-z]", "").length());
    }
}
```

### Sample Output

```text
Number of Uppercase Characters: 7
```

---

### Question 7

**Problem:**  
Write a Java program to print the **number of Lowercase Characters** in the given string.

### Java Code

```java
public class P7 {
    public static void main(String[] args) {

        String str = "MeThodOverLoAdiNG";

        System.out.println("Number of Lowercase Characters: "
                + str.replaceAll("[A-Z]", "").length());
    }
}
```

### Sample Output

```text
Number of Lowercase Characters: 10
```

---

### Question 8

**Problem:**  
Write a Java program to print the **number of Consonants** in the given string.

### Java Code

```java
public class P8 {
    public static void main(String[] args) {

        String str = "MeThodOverLoAdiNG";

        System.out.println("Number of Consonants: "
                + str.replaceAll("[aeiouAEIOU]", "").length());
    }
}
```

### Sample Output

```text
Number of Consonants: 11
```
````

````markdown
### Question 9

**Problem:**  
Write a Java program to **reverse a given string**.

### Java Code

```java
public class P9 {
    public static void main(String[] args) {

        String str = "java";
        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev = rev + str.charAt(i);
        }

        System.out.println("Reversed String: " + rev);
    }
}
```

### Sample Output

```text
Reversed String: avaj
```
````

````markdown
### Question 10

**Problem:**  
Write a Java program to check whether the given string is a **Palindrome**.

### Java Code

```java
public class P10 {
    public static void main(String[] args) {

        String str = "madam";
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
madam is a Palindrome.
```
````

````markdown
### Question 21

**Problem:**  
Write a Java program to check whether a string contains only digits using `replaceAll()`.

### Java Code

```java
public class P21 {
    public static void main(String[] args) {

        String str = "234543";

        if (str.replaceAll("[0-9]", "").isEmpty()) {
            System.out.println("String contains only digits.");
        } else {
            System.out.println("String does not contain only digits.");
        }
    }
}
```

### Sample Output

```text
String contains only digits.
```

---

### Question 22

**Problem:**  
Write a Java program to check whether a string contains only alphabets using `replaceAll()`.

### Java Code

```java
public class P22 {
    public static void main(String[] args) {

        String str = "Java";

        if (str.replaceAll("[a-zA-Z]", "").isEmpty()) {
            System.out.println("String contains only alphabets.");
        } else {
            System.out.println("String does not contain only alphabets.");
        }
    }
}
```

### Sample Output

```text
String contains only alphabets.
```

---

### Question 23

**Problem:**  
Write a Java program to check whether a string is alphanumeric using `replaceAll()`.

### Java Code

```java
public class P23 {
    public static void main(String[] args) {

        String str = "h43ii";

        if (str.replaceAll("[a-zA-Z0-9]", "").isEmpty()) {
            System.out.println("String is Alphanumeric.");
        } else {
            System.out.println("String is Not Alphanumeric.");
        }
    }
}
```

### Sample Output

```text
String is Alphanumeric.
```

---

### Question 24

**Problem:**  
Write a Java program to remove all characters except vowels using `replaceAll()`.

### Java Code

```java
public class P24 {
    public static void main(String[] args) {

        String str = "Java Programming";

        System.out.println(str.replaceAll("[^aeiouAEIOU]", ""));
    }
}
```

### Sample Output

```text
aaoai
```

---

### Question 25

**Problem:**  
Write a Java program to replace every special character with `@` using `replaceAll()`.

### Java Code

```java
public class P25 {
    public static void main(String[] args) {

        String str = "Java@123#Program!";

        System.out.println(str.replaceAll("[a-zA-Z0-9]", "@"));
    }
}
```

### Sample Output

```text
@@@@@ @@@ @@@@@@@
```

---

### Question 26

**Problem:**  
Write a Java program to count the number of special characters using `replaceAll()`.

### Java Code

```java
public class P26 {
    public static void main(String[] args) {

        String str = "Java@123#Program!";

        System.out.println("Number of Special Characters: "
                + str.replaceAll("[a-zA-Z0-9]", "").length());
    }
}
```

### Sample Output

```text
Number of Special Characters: 3
```

---

### Question 27

**Problem:**  
Write a Java program to count the number of alphabets using `replaceAll()`.

### Java Code

```java
public class P27 {
    public static void main(String[] args) {

        String str = "Java123Programming";

        System.out.println("Number of Alphabets: "
                + str.replaceAll("[^a-zA-Z]", "").length());
    }
}
```

### Sample Output

```text
Number of Alphabets: 15
```

---

### Question 28

**Problem:**  
Write a Java program to count the number of uppercase letters using `replaceAll()`.

### Java Code

```java
public class P28 {
    public static void main(String[] args) {

        String str = "JavaPROgramming";

        System.out.println("Number of Uppercase Letters: "
                + str.replaceAll("[^A-Z]", "").length());
    }
}
```

### Sample Output

```text
Number of Uppercase Letters: 4
```

---

### Question 29

**Problem:**  
Write a Java program to count the number of lowercase letters using `replaceAll()`.

### Java Code

```java
public class P29 {
    public static void main(String[] args) {

        String str = "JavaPROgramming";

        System.out.println("Number of Lowercase Letters: "
                + str.replaceAll("[^a-z]", "").length());
    }
}
```

### Sample Output

```text
Number of Lowercase Letters: 11
```

---

### Question 30

**Problem:**  
Write a Java program to remove all occurrences of a specific word using `replaceAll()`.

### Java Code

```java
public class P30 {
    public static void main(String[] args) {

        String str = "Java is easy and Java is powerful";

        System.out.println(str.replaceAll("Java", ""));
    }
}
```

### Sample Output

```text
 is easy and  is powerful
```
````

````markdown
### Question 12

**Problem:**  
Write a Java program to remove all **lowercase letters** from a string using `replaceAll()`.

### Java Code

```java
public class P12 {
    public static void main(String[] args) {

        String str = "hHIi hHelL100";

        System.out.println(str.replaceAll("[a-z]", ""));
    }
}
```

### Sample Output

```text
HI HL100
```

---

### Question 13

**Problem:**  
Write a Java program to extract only **special characters** from a string using `replaceAll()`.

### Java Code

```java
public class P13 {
    public static void main(String[] args) {

        String str = "h234e^&*1lo";

        System.out.println(str.replaceAll("[a-zA-Z0-9]", ""));
    }
}
```

### Sample Output

```text
^&*
```

---

### Question 14

**Problem:**  
Write a Java program to replace every **non-alphabet character with a space** using `replaceAll()`.

### Java Code

```java
public class P14 {
    public static void main(String[] args) {

        String str = "hi!@#23";

        System.out.println(str.replaceAll("[^a-zA-Z]", " "));
    }
}
```

### Sample Output

```text
hi     
```

---

### Question 15

**Problem:**  
Write a Java program to count the **number of digits** present in a string using `replaceAll()`.

### Java Code

```java
public class P15 {
    public static void main(String[] args) {

        String str = "h234ello";

        System.out.println("Number of Digits: "
                + str.replaceAll("[^0-9]", "").length());
    }
}
```

### Sample Output

```text
Number of Digits: 3
```

---

### Question 16

**Problem:**  
Write a Java program to remove all **vowels** from a string using `replaceAll()`.

### Java Code

```java
public class P16 {
    public static void main(String[] args) {

        String str = "Java Programming";

        System.out.println(str.replaceAll("[aeiouAEIOU]", ""));
    }
}
```

### Sample Output

```text
Jv Prgrmmng
```

---

### Question 17

**Problem:**  
Write a Java program to remove all **consonants** from a string using `replaceAll()`.

### Java Code

```java
public class P17 {
    public static void main(String[] args) {

        String str = "Java Programming";

        System.out.println(str.replaceAll("[b-df-hj-np-tv-zB-DF-HJ-NP-TV-Z]", ""));
    }
}
```

### Sample Output

```text
aa oai
```

---

### Question 18

**Problem:**  
Write a Java program to replace all **whitespace characters (spaces, tabs, and newlines)** with `@` using `replaceAll()`.

### Java Code

```java
public class P18 {
    public static void main(String[] args) {

        String str = "Java \t Programming \n Language";

        System.out.println(str.replaceAll("\\s", "@"));
    }
}
```

### Sample Output

```text
Java@@@Programming@@@Language
```
````



