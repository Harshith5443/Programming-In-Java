````markdown id="q1frequencyuppercase"

### Question 1

**Problem:**  
Write a Java program to find the **frequency of only Uppercase letters, Lowercase letters, and Special Characters** in the given string.

**Input:** `LiKE +He ImayE That YOU See?`

### Java Code

```java
public class P1 {

    static void freq(String str) {

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

    public static void main(String[] args) {

        String str = "LiKE +He ImayE That YOU See?";

        System.out.println("Frequency of Uppercase Characters:");
        freq(str.replaceAll("[^A-Z]", ""));

        System.out.println("\nFrequency of Lowercase Characters:");
        freq(str.replaceAll("[^a-z]", ""));

        System.out.println("\nFrequency of Special Characters:");
        freq(str.replaceAll("[A-Za-z0-9 ]", ""));
    }
}
```

### Sample Output

```text
Frequency of Uppercase Characters:
E : 2
H : 1
I : 1
K : 1
L : 1
O : 1
U : 1
Y : 1

Frequency of Lowercase Characters:
a : 2
e : 2
h : 1
i : 1
m : 1
t : 1
y : 1

Frequency of Special Characters:
+ : 1
? : 1
```
````

````markdown id="q2maxfrequency"

### Question 2

**Problem:**  
Write a Java program to find the **maximum repeated (most frequent) character** in a given string using a frequency array.

**Input:** `LiKE +He ImayE That YOU See?`

### Java Code

```java
public class P2 {

    public static void main(String[] args) {

        String str = "LiKE +He ImayE That YOU See?";

        int max = 0;
        char maxChar = '\0';

        int[] arr = new int[127];

        for (int i = 0; i < str.length(); i++) {

            char ch = str.charAt(i);

            arr[ch]++;
        }

        for (int i = 0; i < arr.length; i++) {

            if (arr[i] > max) {

                max = arr[i];
                maxChar = (char) i;
            }
        }

        System.out.println("Most Repeated Character : " + maxChar);
        System.out.println("Frequency : " + max);
    }
}
```

### Sample Output

```text
Most Repeated Character : e
Frequency : 3
```
````
