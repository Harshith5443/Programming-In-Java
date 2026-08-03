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

````markdown id="q3largestpalindromicsubstring"

### Question 3

**Problem:**  
Write a Java program to find the **largest palindromic substring** in a given string.

**Input:** `aabbad`

### Java Code

```java
public class P3 {

    static boolean isPalindrome(String str) {

        int i = 0;
        int j = str.length() - 1;

        while (i < j) {

            if (str.charAt(i) != str.charAt(j)) {

                return false;
            }

            i++;
            j--;
        }

        return true;
    }

    public static void main(String[] args) {

        String str = "aabbad";

        String max = "";

        for (int i = 0; i < str.length(); i++) {

            for (int j = i + 1; j <= str.length(); j++) {

                String temp = str.substring(i, j);

                if (isPalindrome(temp) && temp.length() > max.length()) {

                    max = temp;
                }
            }
        }

        System.out.println("Largest Palindromic Substring : " + max);
        System.out.println("Length : " + max.length());
    }
}
```

### Sample Output

```text
Largest Palindromic Substring : abba
Length : 4
```
````

````markdown id="q5anagramfrequency"

### Question 5

**Problem:**  
Write a Java program to check whether two given strings are **Anagrams** or not using a frequency array.

**Input:**  
String 1: `listen`  
String 2: `silent`

### Java Code

```java
public class P5 {

    public static void main(String[] args) {

        String str1 = "listen";
        String str2 = "silent";

        int[] arr = new int[127];

        for (int i = 0; i < str1.length(); i++) {

            char ch = str1.charAt(i);

            arr[ch]++;
        }

        for (int i = 0; i < str2.length(); i++) {

            char ch = str2.charAt(i);

            arr[ch]--;
        }

        for (int i = 0; i < arr.length; i++) {

            if (arr[i] != 0) {

                System.out.println("Not Anagram");
                return;
            }
        }

        System.out.println("Anagram");
    }
}
```

### Sample Output

```text
Anagram
```
````

````markdown id="q1sumevendigits"

### Question 1

**Problem:**  
Write a Java program to find the **sum of only even digits** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P1 {
    public static void main(String[] args) {

        int num = 948216083;

        int sum = 0;

        while (num > 0) {

            int rem = num % 10;

            if (rem % 2 == 0) {

                sum += rem;
            }

            num = num / 10;
        }

        System.out.println("Sum of Even Digits : " + sum);
    }
}
```

### Sample Output

```text
Sum of Even Digits : 20
```
````

````markdown id="q2sumodddigits"

### Question 2

**Problem:**  
Write a Java program to find the **sum of only odd digits** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P2 {
    public static void main(String[] args) {

        int num = 948216083;

        int sum = 0;

        while (num > 0) {

            int rem = num % 10;

            if (rem % 2 != 0) {

                sum += rem;
            }

            num = num / 10;
        }

        System.out.println("Sum of Odd Digits : " + sum);
    }
}
```

### Sample Output

```text
Sum of Odd Digits : 21
```
````
````markdown id="q3multiplyevendigits"

### Question 3

**Problem:**  
Write a Java program to find the **product of only even digits** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P3 {
    public static void main(String[] args) {

        int num = 948216083;

        int product = 1;

        while (num > 0) {

            int rem = num % 10;

            if (rem % 2 == 0) {

                product *= rem;
            }

            num = num / 10;
        }

        System.out.println("Product of Even Digits : " + product);
    }
}
```

### Sample Output

```text
Product of Even Digits : 384
```
````
````markdown id="q4multiplyodddigits"

### Question 4

**Problem:**  
Write a Java program to find the **product of only odd digits** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P4 {
    public static void main(String[] args) {

        int num = 948216083;

        int product = 1;

        while (num > 0) {

            int rem = num % 10;

            if (rem % 2 != 0) {

                product *= rem;
            }

            num = num / 10;
        }

        System.out.println("Product of Odd Digits : " + product);
    }
}
```

### Sample Output

```text
Product of Odd Digits : 27
```
````
````markdown id="q5countevendigits"

### Question 5

**Problem:**  
Write a Java program to **count the number of even digits** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P5 {
    public static void main(String[] args) {

        int num = 948216083;

        int count = 0;

        while (num > 0) {

            int rem = num % 10;

            if (rem % 2 == 0) {

                count++;
            }

            num = num / 10;
        }

        System.out.println("Count of Even Digits : " + count);
    }
}
```

### Sample Output

```text
Count of Even Digits : 5
```
````
````markdown id="q6countodddigits"

### Question 6

**Problem:**  
Write a Java program to **count the number of odd digits** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P6 {
    public static void main(String[] args) {

        int num = 948216083;

        int count = 0;

        while (num > 0) {

            int rem = num % 10;

            if (rem % 2 != 0) {

                count++;
            }

            num = num / 10;
        }

        System.out.println("Count of Odd Digits : " + count);
    }
}
```

### Sample Output

```text
Count of Odd Digits : 4
```
````
````markdown id="q7count8digits"

### Question 7

**Problem:**  
Write a Java program to **count how many times the digit `8` appears** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P7 {
    public static void main(String[] args) {

        int num = 948216083;

        int count = 0;

        while (num > 0) {

            int rem = num % 10;

            if (rem == 8) {

                count++;
            }

            num = num / 10;
        }

        System.out.println("Count of 8's : " + count);
    }
}
```

### Sample Output

```text
Count of 8's : 2
```
````
````markdown id="q8countdivisibleby2and3"

### Question 8

**Problem:**  
Write a Java program to **count the digits divisible by both 2 and 3** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P8 {
    public static void main(String[] args) {

        int num = 948216083;

        int count = 0;

        while (num > 0) {

            int rem = num % 10;

            if (rem != 0 && rem % 2 == 0 && rem % 3 == 0) {

                count++;
            }

            num = num / 10;
        }

        System.out.println("Count of Digits Divisible by 2 and 3 : " + count);
    }
}
```

### Sample Output

```text
Count of Digits Divisible by 2 and 3 : 1
```
````
````markdown id="q9sumdivisibleby9"

### Question 9

**Problem:**  
Write a Java program to **find the sum of the digits divisible by 9** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P9 {
    public static void main(String[] args) {

        int num = 948216083;

        int sum = 0;

        while (num > 0) {

            int rem = num % 10;

            if (rem % 9 == 0) {

                sum += rem;
            }

            num = num / 10;
        }

        System.out.println("Sum of Digits Divisible by 9 : " + sum);
    }
}
```

### Sample Output

```text
Sum of Digits Divisible by 9 : 9
```
````
````markdown id="q10sumdivisibleby4"

### Question 10

**Problem:**  
Write a Java program to **find the sum of the digits divisible by 4** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P10 {
    public static void main(String[] args) {

        int num = 948216083;

        int sum = 0;

        while (num > 0) {

            int rem = num % 10;

            if (rem != 0 && rem % 4 == 0) {

                sum += rem;
            }

            num = num / 10;
        }

        System.out.println("Sum of Digits Divisible by 4 : " + sum);
    }
}
```

### Sample Output

```text
Sum of Digits Divisible by 4 : 20
```
````
````markdown id="q11sumdivisibleby2"

### Question 11

**Problem:**  
Write a Java program to **find the sum of the digits divisible by 2** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P11 {
    public static void main(String[] args) {

        int num = 948216083;

        int sum = 0;

        while (num > 0) {

            int rem = num % 10;

            if (rem % 2 == 0) {

                sum += rem;
            }

            num = num / 10;
        }

        System.out.println("Sum of Digits Divisible by 2 : " + sum);
    }
}
```

### Sample Output

```text
Sum of Digits Divisible by 2 : 20
```
````
````markdown id="q12multiplydivisibleby9"

### Question 12

**Problem:**  
Write a Java program to **find the product of the digits divisible by 9** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P12 {
    public static void main(String[] args) {

        int num = 948216083;

        int product = 1;

        while (num > 0) {

            int rem = num % 10;

            if (rem != 0 && rem % 9 == 0) {

                product *= rem;
            }

            num = num / 10;
        }

        System.out.println("Product of Digits Divisible by 9 : " + product);
    }
}
```

### Sample Output

```text
Product of Digits Divisible by 9 : 9
```
````

````markdown id="q13multiplydivisibleby4"

### Question 13

**Problem:**  
Write a Java program to **find the product of the digits divisible by 4** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P13 {
    public static void main(String[] args) {

        int num = 948216083;

        int product = 1;

        while (num > 0) {

            int rem = num % 10;

            if (rem != 0 && rem % 4 == 0) {

                product *= rem;
            }

            num = num / 10;
        }

        System.out.println("Product of Digits Divisible by 4 : " + product);
    }
}
```

### Sample Output

```text
Product of Digits Divisible by 4 : 256
```
````
````markdown id="q14multiplydivisibleby2"

### Question 14

**Problem:**  
Write a Java program to **find the product of the digits divisible by 2** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P14 {
    public static void main(String[] args) {

        int num = 948216083;

        int product = 1;

        while (num > 0) {

            int rem = num % 10;

            if (rem % 2 == 0) {

                product *= rem;
            }

            num = num / 10;
        }

        System.out.println("Product of Digits Divisible by 2 : " + product);
    }
}
```

### Sample Output

```text
Product of Digits Divisible by 2 : 384
```
````
````markdown id="q15sumevenmultiplyodd"

### Question 15

**Problem:**  
Write a Java program to:

1. Find the **sum of all even digits**.
2. Find the **product of all odd digits**.

**Input:** `948216083`

### Java Code

```java
public class P15 {
    public static void main(String[] args) {

        int num = 948216083;

        int evenSum = 0;
        int oddProduct = 1;

        while (num > 0) {

            int rem = num % 10;

            if (rem % 2 == 0) {

                evenSum += rem;

            } else {

                oddProduct *= rem;
            }

            num = num / 10;
        }

        System.out.println("Sum of Even Digits : " + evenSum);
        System.out.println("Product of Odd Digits : " + oddProduct);
    }
}
```

### Sample Output

```text
Sum of Even Digits : 28
Product of Odd Digits : 27
```
````
````markdown id="q16sumdiv2multiplydiv3"

### Question 16

**Problem:**  
Write a Java program to:

1. Find the **sum of digits divisible by 2**.
2. Find the **product of digits divisible by 3**.

**Input:** `948216083`

### Java Code

```java
public class P16 {
    public static void main(String[] args) {

        int num = 948216083;

        int sum = 0;
        int product = 1;

        while (num > 0) {

            int rem = num % 10;

            if (rem % 2 == 0) {

                sum += rem;
            }

            if (rem != 0 && rem % 3 == 0) {

                product *= rem;
            }

            num = num / 10;
        }

        System.out.println("Sum of Digits Divisible by 2 : " + sum);
        System.out.println("Product of Digits Divisible by 3 : " + product);
    }
}
```

### Sample Output

```text
Sum of Digits Divisible by 2 : 28
Product of Digits Divisible by 3 : 162
```
````
````markdown id="q17squaredivisibleby3"

### Question 17

**Problem:**  
Write a Java program to **find the square of the digits that are divisible by 3** in the given number.

**Input:** `948216083`

### Java Code

```java
public class P17 {
    public static void main(String[] args) {

        int num = 948216083;

        while (num > 0) {

            int rem = num % 10;

            if (rem != 0 && rem % 3 == 0) {

                System.out.println(rem + " -> " + (rem * rem));
            }

            num = num / 10;
        }
    }
}
```

### Sample Output

```text
3 -> 9
6 -> 36
9 -> 81
```
````
````markdown id="q18maxmindigit"

### Question 18

**Problem:**  
Write a Java program to find the **maximum** and **minimum** digit in the given number.

**Input:** `948216083`

### Java Code

```java
public class P18 {
    public static void main(String[] args) {

        int num = 948216083;

        int max = 0;
        int min = 9;

        while (num > 0) {

            int rem = num % 10;

            if (rem > max) {

                max = rem;
            }

            if (rem < min) {

                min = rem;
            }

            num = num / 10;
        }

        System.out.println("Maximum Digit : " + max);
        System.out.println("Minimum Digit : " + min);
    }
}
```

### Sample Output

```text
Maximum Digit : 9
Minimum Digit : 0
```
````
