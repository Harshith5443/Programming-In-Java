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

````markdown id="q4stringoperations"

### Question 4

**Problem:**  
Write a Java program to perform the following string operations:

1. Print the original string.
2. Extract vowels and consonants.
3. Reverse only the vowels.
4. Reverse both vowels and consonants.
5. Reverse only the consonants.
6. Count vowels and consonants.
7. Reverse the first half of the string.
8. Reverse the second half of the string.

**Input:** `Methodoverloading`

### Java Code

```java
public class P4 {

    static String reverse(String str) {

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

        String str = "Methodoverloading";

        System.out.println("The String is : " + str);

        String vowels = str.replaceAll("[^aeiouAEIOU]", "");
        String consonants = str.replaceAll("[aeiouAEIOU]", "");

        System.out.println("Vowels : " + vowels + "    Consonants : " + consonants);

        System.out.println("Reverse Vowels : " + reverse(vowels) + "    Consonants : " + consonants);

        System.out.println("Reverse Vowels : " + reverse(vowels)
                + "    Reverse Consonants : " + reverse(consonants));

        System.out.println("Vowels : " + vowels
                + "    Reverse Consonants : " + reverse(consonants));

        System.out.println("Vowels Length : " + vowels.length()
                + "    Consonants Length : " + consonants.length());

        System.out.println("1st Half String Reverse : "
                + reverse(str.substring(0, str.length() / 2))
                + str.substring(str.length() / 2));

        System.out.println("2nd Half String Reverse : "
                + str.substring(0, str.length() / 2)
                + reverse(str.substring(str.length() / 2)));
    }
}
```

### Sample Output

```text
The String is : Methodoverloading
Vowels : eooeaia    Consonants : Mthdvrldng
Reverse Vowels : aiaeooe    Consonants : Mthdvrldng
Reverse Vowels : aiaeooe    Reverse Consonants : gndlrvdhtM
Vowels : eooeaia    Reverse Consonants : gndlrvdhtM
Vowels Length : 7    Consonants Length : 10
1st Half String Reverse : revodohteMloading
2nd Half String Reverse : Methodovegnidaolr
```
````

````markdown id="q5asciiencryption"

### Question 5

**Problem:**  
Write a Java program to convert the string **"hello"** into **"lipps"** using **ASCII values** (each character is shifted by +4).

**Input:** `hello`

### Java Code

```java
public class P5 {
    public static void main(String[] args) {

        String str = "hello";
        String result = "";

        for (int i = 0; i < str.length(); i++) {

            char ch = str.charAt(i);

            result += (char) (ch + 4);
        }

        System.out.println("Original String : " + str);
        System.out.println("Encrypted String : " + result);
    }
}
```

### Sample Output

```text
Original String : hello
Encrypted String : lipps
```
````

````markdown id="q6charfrequencyarray"

### Question 6

**Problem:**  
Write a Java program to **count the frequency of each character** in a given string using an array.

**Input:** `aabbccdd`

### Java Code

```java
public class P6 {
    public static void main(String[] args) {

        String str = "aabbccdd";

        int[] arr = new int[127];

        for (int i = 0; i < str.length(); i++) {

            char ch = str.charAt(i);

            arr[ch]++;
        }

        for (int i = 0; i < arr.length; i++) {

            if (arr[i] != 0) {

                System.out.println((char) i + " : " + arr[i]);
            }
        }
    }
}
```

### Sample Output

```text
a : 2
b : 2
c : 2
d : 2
```
````


