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

### Question 2

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

````markdown id="q2palignore"

### Question 3

**Problem:**  
Write a Java program to check whether the given string is a **Palindrome** by **ignoring the case**.

**Input:** `Madam`

### Java Code

```java
public class P2 {
    public static void main(String[] args) {

        String str = "Madam";
        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev = rev + str.charAt(i);
        }

        if (str.equalsIgnoreCase(rev)) {
            System.out.println(str + " is a Palindrome.");
        } else {
            System.out.println(str + " is Not a Palindrome.");
        }
    }
}
```

### Sample Output

```text
Madam is a Palindrome.
```
````

````markdown id="q4methods"

### Question 4

**Problem:**  
Write a Java program to **reverse a string** using the following methods:

1. Method Calling (No Parameters, No Return Type)
2. Method with Parameter (No Return Type)
3. Method with Return Type (No Parameters)
4. Method with Parameter and Return Type

---

## 1. Method Calling (No Parameters, No Return Type)

### Java Code

```java
public class P4 {

    static void reverse() {
        String str = "java";
        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        System.out.println("Reversed String: " + rev);
    }

    public static void main(String[] args) {
        reverse();
    }
}
```

### Sample Output

```text
Reversed String: avaj
```

---

## 2. Method with Parameter (No Return Type)

### Java Code

```java
public class P4 {

    static void reverse(String str) {

        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        System.out.println("Reversed String: " + rev);
    }

    public static void main(String[] args) {

        reverse("java");
    }
}
```

### Sample Output

```text
Reversed String: avaj
```

---

## 3. Method with Return Type (No Parameter)

### Java Code

```java
public class P4 {

    static String reverse() {

        String str = "java";
        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        return rev;
    }

    public static void main(String[] args) {

        System.out.println("Reversed String: " + reverse());
    }
}
```

### Sample Output

```text
Reversed String: avaj
```

---

## 4. Method with Parameter and Return Type

### Java Code

```java
public class P4 {

    static String reverse(String str) {

        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        return rev;
    }

    public static void main(String[] args) {

        System.out.println("Reversed String: " + reverse("java"));
    }
}
```

### Sample Output

```text
Reversed String: avaj
```

---

# Non-Static Version

## Method with Parameter and Return Type (Non-Static)

### Java Code

```java
public class P4 {

    String reverse(String str) {

        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        return rev;
    }

    public static void main(String[] args) {

        P4 obj = new P4();

        System.out.println("Reversed String: " + obj.reverse("java"));
    }
}
```

### Sample Output

```text
Reversed String: avaj
```
````

````markdown id="q5palmethods"

### Question 5

**Problem:**  
Write a Java program to check whether a given string is a **Palindrome** using the following methods:

1. Method Calling (No Parameters, No Return Type)
2. Method with Parameter (No Return Type)
3. Method with Return Type (No Parameters)
4. Method with Parameter and Return Type

---

## 1. Method Calling (No Parameters, No Return Type)

### Java Code

```java
public class P5 {

    static void palindrome() {

        String str = "madam";
        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        if (str.equals(rev)) {
            System.out.println(str + " is a Palindrome.");
        } else {
            System.out.println(str + " is Not a Palindrome.");
        }
    }

    public static void main(String[] args) {

        palindrome();
    }
}
```

### Sample Output

```text
madam is a Palindrome.
```

---

## 2. Method with Parameter (No Return Type)

### Java Code

```java
public class P5 {

    static void palindrome(String str) {

        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        if (str.equals(rev)) {
            System.out.println(str + " is a Palindrome.");
        } else {
            System.out.println(str + " is Not a Palindrome.");
        }
    }

    public static void main(String[] args) {

        palindrome("madam");
    }
}
```

### Sample Output

```text
madam is a Palindrome.
```

---

## 3. Method with Return Type (No Parameter)

### Java Code

```java
public class P5 {

    static boolean palindrome() {

        String str = "madam";
        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        return str.equals(rev);
    }

    public static void main(String[] args) {

        System.out.println(palindrome() ? "Palindrome" : "Not a Palindrome");
    }
}
```

### Sample Output

```text
Palindrome
```

---

## 4. Method with Parameter and Return Type

### Java Code

```java
public class P5 {

    static boolean palindrome(String str) {

        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        return str.equals(rev);
    }

    public static void main(String[] args) {

        String str = "madam";

        System.out.println(palindrome(str) ? "Palindrome" : "Not a Palindrome");
    }
}
```

### Sample Output

```text
Palindrome
```

---

# Non-Static Version

## Method with Parameter and Return Type (Non-Static)

### Java Code

```java
public class P5 {

    boolean palindrome(String str) {

        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        return str.equals(rev);
    }

    public static void main(String[] args) {

        P5 obj = new P5();

        String str = "madam";

        System.out.println(obj.palindrome(str) ? "Palindrome" : "Not a Palindrome");
    }
}
```

### Sample Output

```text
Palindrome
```
````

````markdown id="q6swap"

### Question 6

**Problem:**  
Write a Java program to **swap two numbers** using the following methods:

1. With Temporary Variable
2. Without Temporary Variable
3. Using XOR Operator

---

## 1. Swap Using Temporary Variable

### Java Code

```java
public class P6 {
    public static void main(String[] args) {

        int a = 10;
        int b = 20;

        System.out.println("Before Swapping:");
        System.out.println("a = " + a);
        System.out.println("b = " + b);

        int temp = a;
        a = b;
        b = temp;

        System.out.println("After Swapping:");
        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}
```

### Sample Output

```text
Before Swapping:
a = 10
b = 20
After Swapping:
a = 20
b = 10
```

---

## 2. Swap Without Temporary Variable

### Java Code

```java
public class P6 {
    public static void main(String[] args) {

        int a = 10;
        int b = 20;

        System.out.println("Before Swapping:");
        System.out.println("a = " + a);
        System.out.println("b = " + b);

        a = a + b;
        b = a - b;
        a = a - b;

        System.out.println("After Swapping:");
        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}
```

### Sample Output

```text
Before Swapping:
a = 10
b = 20
After Swapping:
a = 20
b = 10
```

---

## 3. Swap Using XOR Operator

### Java Code

```java
public class P6 {
    public static void main(String[] args) {

        int a = 10;
        int b = 20;

        System.out.println("Before Swapping:");
        System.out.println("a = " + a);
        System.out.println("b = " + b);

        a = a ^ b;
        b = a ^ b;
        a = a ^ b;

        System.out.println("After Swapping:");
        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}
```

### Sample Output

```text
Before Swapping:
a = 10
b = 20
After Swapping:
a = 20
b = 10
```
````

````markdown id="q7reversewithoutcharat"

### Question 7

**Problem:**  
Write a Java program to **reverse a string without using `charAt()`**.

**Input:** `method`

### Java Code

```java
public class P7 {
    public static void main(String[] args) {

        String str = "method";

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

        System.out.println("Original String: " + str);
        System.out.println("Reversed String: " + new String(ch));
    }
}
```

### Sample Output

```text
Original String: method
Reversed String: dohtem
```
````

````markdown id="q8palindromecharat"

### Question 8

**Problem:**  
Write a Java program to check whether a given string is a **Palindrome** using the `charAt()` method.

**Input:** `level`

### Java Code

```java
public class P8 {
    public static void main(String[] args) {

        String str = "level";

        int i = 0;
        int j = str.length() - 1;

        while (i < j) {

            if (str.charAt(i) != str.charAt(j)) {
                System.out.println("Not a Palindrome");
                return;
            }

            i++;
            j--;
        }

        System.out.println("Palindrome");
    }
}
```

### Sample Output

```text
Palindrome
```
````
````markdown id="q9vowelboolean"

### Question 9

**Problem:**  
Write a Java program to check whether the given character is a **Vowel** or not using a **boolean method**.

**Input:** `A`

### Java Code

```java
public class P9 {

    static boolean isVowel(char ch) {

        return ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U'
            || ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u';
    }

    public static void main(String[] args) {

        char ch = 'A';

        System.out.println(isVowel(ch));
    }
}
```

### Sample Output

```text
true
```
````

````markdown id="q9vowelboolean"

### Question 9

**Problem:**  
Write a Java program to check whether the given character is a **Vowel** or not using a **boolean method**.

**Input:** `A`

### Java Code

```java
public class P9 {

    static boolean isVowel(char ch) {

        if (ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U'
                || ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {

            return true;

        } else {

            return false;
        }
    }

    public static void main(String[] args) {

        char ch = 'A';

        System.out.println(isVowel(ch));
    }
}
```

### Sample Output

```text
true
```
````
````markdown id="q10consonantboolean"

### Question 10

**Problem:**  
Write a Java program to check whether the given character is a **Consonant** or not using a **boolean method**.

**Input:** `B`

### Java Code

```java
public class P10 {

    static boolean isConsonant(char ch) {

        if (Character.isLetter(ch) &&
            !(ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U'
           || ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u')) {

            return true;

        } else {

            return false;
        }
    }

    public static void main(String[] args) {

        char ch = 'B';

        System.out.println(isConsonant(ch));
    }
}
```

### Sample Output

```text
true
```
````

````markdown id="q11reversevowels"

### Question 11

**Problem:**  
Write a Java program to **reverse only the vowels** in a given string.

**Input:** `Method`

### Java Code

```java
public class P11 {

    static boolean isVowel(char ch) {

        return ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U'
            || ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u';
    }

    public static void main(String[] args) {

        String str = "Method";

        char[] ch = str.toCharArray();

        int i = 0;
        int j = ch.length - 1;

        while (i < j) {

            while (i < j && !isVowel(ch[i])) {
                i++;
            }

            while (i < j && !isVowel(ch[j])) {
                j--;
            }

            char temp = ch[i];
            ch[i] = ch[j];
            ch[j] = temp;

            i++;
            j--;
        }

        System.out.println("Original String: " + str);
        System.out.println("Modified String: " + new String(ch));
    }
}
```

### Sample Output

```text
Original String: Method
Modified String: Mothed
```
````
````markdown id="q12reverseconsonants"

### Question 12

**Problem:**  
Write a Java program to **reverse only the consonants** in a given string.

**Input:** `hello`

### Java Code

```java
public class P12 {

    static boolean isConsonant(char ch) {

        return Character.isLetter(ch) &&
               (ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U'
              || ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u');
    }

    public static void main(String[] args) {

        String str = "hello";

        char[] ch = str.toCharArray();

        int i = 0;
        int j = ch.length - 1;

        while (i < j) {

            while (i < j && isConsonant(ch[i])) {
                i++;
            }

            while (i < j && isConsonant(ch[j])) {
                j--;
            }

            char temp = ch[i];
            ch[i] = ch[j];
            ch[j] = temp;

            i++;
            j--;
        }

        System.out.println("Original String: " + str);
        System.out.println("Modified String: " + new String(ch));
    }
}
```

### Sample Output

```text
Original String: hello
Modified String: lelho
```
````

````markdown id="q13reversealphabets"

### Question 13

**Problem:**  
Write a Java program to **reverse only the alphabets** in a given string.

**Input:** `a1b2c3`

### Java Code

```java
public class P13 {

    static boolean isLetter(char ch) {

        return (ch >= 'a' && ch <= 'z') ||
               (ch >= 'A' && ch <= 'Z');
    }

    public static void main(String[] args) {

        String str = "a1b2c3";

        char[] ch = str.toCharArray();

        int i = 0;
        int j = ch.length - 1;

        while (i < j) {

            while (i < j && !isLetter(ch[i])) {
                i++;
            }

            while (i < j && !isLetter(ch[j])) {
                j--;
            }

            char temp = ch[i];
            ch[i] = ch[j];
            ch[j] = temp;

            i++;
            j--;
        }

        System.out.println("Original String: " + str);
        System.out.println("Modified String: " + new String(ch));
    }
}
```

### Sample Output

```text
Original String: a1b2c3
Modified String: c1b2a3
```
````

````markdown id="q14reverseuppercase"

### Question 14

**Problem:**  
Write a Java program to **reverse only the uppercase characters** in a given string.

**Input:** `JaVaPrOgRaM`

### Java Code

```java
public class P14 {

    static boolean isUpper(char ch) {

        return ch >= 'A' && ch <= 'Z';
    }

    public static void main(String[] args) {

        String str = "JaVaPrOgRaM";

        char[] ch = str.toCharArray();

        int i = 0;
        int j = ch.length - 1;

        while (i < j) {

            while (i < j && !isUpper(ch[i])) {
                i++;
            }

            while (i < j && !isUpper(ch[j])) {
                j--;
            }

            char temp = ch[i];
            ch[i] = ch[j];
            ch[j] = temp;

            i++;
            j--;
        }

        System.out.println("Original String: " + str);
        System.out.println("Modified String: " + new String(ch));
    }
}
```

### Sample Output

```text
Original String: JaVaPrOgRaM
Modified String: MaRgOrPaVaJ
```
````

````markdown id="q15reverselowercase"

### Question 15

**Problem:**  
Write a Java program to **reverse only the lowercase characters** in a given string.

**Input:** `JaVaPrOgRaM`

### Java Code

```java
public class P15 {

    static boolean isLower(char ch) {

        return ch >= 'a' && ch <= 'z';
    }

    public static void main(String[] args) {

        String str = "JaVaPrOgRaM";

        char[] ch = str.toCharArray();

        int i = 0;
        int j = ch.length - 1;

        while (i < j) {

            while (i < j && !isLower(ch[i])) {
                i++;
            }

            while (i < j && !isLower(ch[j])) {
                j--;
            }

            char temp = ch[i];
            ch[i] = ch[j];
            ch[j] = temp;

            i++;
            j--;
        }

        System.out.println("Original String: " + str);
        System.out.println("Modified String: " + new String(ch));
    }
}
```

### Sample Output

```text
Original String: JaVaPrOgRaM
Modified String: JrAgOrPaVaM
```
````

````markdown id="palindromeprograms"

# Palindrome Programs

---

### Question 1

**Problem:**  
Write a Java program to check whether a given string is a **Palindrome**.

**Input:** `madam`

### Java Code

```java
public class P1 {
    public static void main(String[] args) {

        String str = "madam";
        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        if (str.equals(rev)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a Palindrome");
        }
    }
}
```

### Sample Output

```text
Palindrome
```

---

### Question 2

**Problem:**  
Write a Java program to check whether a given string is a **Palindrome** using **Two Pointers**.

**Input:** `level`

### Java Code

```java
public class P2 {
    public static void main(String[] args) {

        String str = "level";

        int i = 0;
        int j = str.length() - 1;

        while (i < j) {

            if (str.charAt(i) != str.charAt(j)) {
                System.out.println("Not a Palindrome");
                return;
            }

            i++;
            j--;
        }

        System.out.println("Palindrome");
    }
}
```

### Sample Output

```text
Palindrome
```

---

### Question 3

**Problem:**  
Write a Java program to check whether a given string is a **Palindrome** by ignoring the **case**.

**Input:** `Madam`

### Java Code

```java
public class P3 {
    public static void main(String[] args) {

        String str = "Madam";
        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        if (str.equalsIgnoreCase(rev)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a Palindrome");
        }
    }
}
```

### Sample Output

```text
Palindrome
```

---

### Question 4

**Problem:**  
Write a Java program to check whether a given string is a **Palindrome** by ignoring **spaces**.

**Input:** `nurses run`

### Java Code

```java
public class P4 {
    public static void main(String[] args) {

        String str = "nurses run";

        str = str.replace(" ", "");

        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        if (str.equals(rev)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a Palindrome");
        }
    }
}
```

### Sample Output

```text
Palindrome
```

---

### Question 5

**Problem:**  
Write a Java program to check whether a given string is a **Palindrome** by ignoring **spaces and case**.

**Input:** `Never Odd Or Even`

### Java Code

```java
public class P5 {
    public static void main(String[] args) {

        String str = "Never Odd Or Even";

        str = str.replace(" ", "").toLowerCase();

        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        if (str.equals(rev)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a Palindrome");
        }
    }
}
```

### Sample Output

```text
Palindrome
```

---

### Question 6

**Problem:**  
Write a Java program to check whether a given string is a **Palindrome** by ignoring **special characters**.

**Input:** `madam !!`

### Java Code

```java
public class P6 {
    public static void main(String[] args) {

        String str = "madam !!";

        str = str.replaceAll("[^a-zA-Z0-9]", "");

        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        if (str.equalsIgnoreCase(rev)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a Palindrome");
        }
    }
}
```

### Sample Output

```text
Palindrome
```

---

### Question 7

**Problem:**  
Write a Java program to **reverse a string and check whether it is a Palindrome**.

**Input:** `radar`

### Java Code

```java
public class P7 {
    public static void main(String[] args) {

        String str = "radar";
        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        System.out.println("Reversed String: " + rev);

        if (str.equals(rev)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a Palindrome");
        }
    }
}
```

### Sample Output

```text
Reversed String: radar
Palindrome
```

````

