
````markdown

### Question 1

**Problem:**  
Write a Java program to **sort an unsorted `ArrayList`** using Bubble Sort.

**Input:**  
ArrayList: `4, 6, 10, 9`

### Java Code

```java
import java.util.ArrayList;
import java.util.Arrays;

public class P1 {
    public static void main(String[] args) {

        ArrayList<Integer> a1 =
                new ArrayList<Integer>(Arrays.asList(4, 6, 10, 9));

        for (int i = 0; i < a1.size(); i++) {

            for (int j = 0; j < a1.size() - 1 - i; j++) {

                if (a1.get(j) > a1.get(j + 1)) {

                    int temp = a1.get(j);

                    a1.set(j, a1.get(j + 1));

                    a1.set(j + 1, temp);
                }
            }
        }

        System.out.println("Sorted ArrayList : " + a1);
    }
}
```

### Sample Output

```text
Sorted ArrayList : [4, 6, 9, 10]
```

````
````markdown
### Question 2

**Problem:**  
Write a Java program to **search an element in an `ArrayList`**.

**Input:**  
ArrayList: `10, 20, 30, 40, 50`  
Search: `30`

### Java Code

```java
import java.util.ArrayList;
import java.util.Arrays;

class MainClass {
    public static void main(String[] args) {

        ArrayList<Integer> a1 =
                new ArrayList<Integer>(Arrays.asList(10, 20, 30, 40, 50));

        int search = 30;

        for (int i = 0; i < a1.size(); i++) {

            if (a1.get(i) == search) {

                System.out.println("Element Found");
                return;
            }
        }

        System.out.println("Element Not Found");
    }
}
```

### Sample Output

```text
Element Found
```

````
````markdown
### Question 3

**Problem:**  
Write a Java program to find the **1st Maximum Number in an `ArrayList`**.

**Input:**  
ArrayList: `30, 20, 10, 40, 50`

### Java Code

```java
import java.util.ArrayList;
import java.util.Arrays;

class MainClass {
    public static void main(String[] args) {

        ArrayList<Integer> a1 =
                new ArrayList<Integer>(Arrays.asList(30, 20, 10, 40, 50));

        int max = Integer.MIN_VALUE;

        for (int no : a1) {

            if (no > max) {

                max = no;
            }
        }

        System.out.println("1st Maximum Number : " + max);
    }
}
```

### Sample Output

```text
1st Maximum Number : 50
```

````
````markdown
### Question 4

**Problem:**  
Write a Java program to find the **2nd Maximum Number in an `ArrayList`**.

**Input:**  
ArrayList: `30, 20, 10, 40, 50`

### Java Code

```java
import java.util.ArrayList;
import java.util.Arrays;

class MainClass {
    public static void main(String[] args) {

        ArrayList<Integer> a1 =
                new ArrayList<Integer>(Arrays.asList(30, 20, 10, 40, 50));

        int max = Integer.MIN_VALUE;
        int secondMax = Integer.MIN_VALUE;

        for (int no : a1) {

            if (no > max) {

                secondMax = max;

                max = no;

            } else if (no > secondMax && no != max) {

                secondMax = no;
            }
        }

        System.out.println("2nd Maximum Number : " + secondMax);
    }
}
```

### Sample Output

```text
2nd Maximum Number : 40
```

````
````markdown
### Question 5

**Problem:**  
Write a Java program to find the **1st Minimum Number in an `ArrayList`**.

**Input:**  
ArrayList: `30, 20, 10, 40, 50`

### Java Code

```java
import java.util.ArrayList;
import java.util.Arrays;

class MainClass {
    public static void main(String[] args) {

        ArrayList<Integer> a1 =
                new ArrayList<Integer>(Arrays.asList(30, 20, 10, 40, 50));

        int min = Integer.MAX_VALUE;

        for (int no : a1) {

            if (no < min) {

                min = no;
            }
        }

        System.out.println("1st Minimum Number : " + min);
    }
}
```

### Sample Output

```text
1st Minimum Number : 10
```

````
````markdown
### Question 6

**Problem:**  
Write a Java program to find the **2nd Minimum Number in an `ArrayList`**.

**Input:**  
ArrayList: `30, 20, 10, 40, 50`

### Java Code

```java
import java.util.ArrayList;
import java.util.Arrays;

class MainClass {
    public static void main(String[] args) {

        ArrayList<Integer> a1 =
                new ArrayList<Integer>(Arrays.asList(30, 20, 10, 40, 50));

        int min = Integer.MAX_VALUE;
        int secondMin = Integer.MAX_VALUE;

        for (int no : a1) {

            if (no < min) {

                secondMin = min;

                min = no;

            } else if (no < secondMin && no != min) {

                secondMin = no;
            }
        }

        System.out.println("2nd Minimum Number : " + secondMin);
    }
}
```

### Sample Output

```text
2nd Minimum Number : 20
```

````
````markdown
### Question 7

**Problem:**  
Write a Java program to find **two elements in an `ArrayList` whose sum is equal to the target**.

**Input:**  
ArrayList: `10, 20, 30, 40, 50`  
Target: `70`

### Java Code

```java
import java.util.ArrayList;
import java.util.Arrays;

class MainClass {
    public static void main(String[] args) {

        ArrayList<Integer> a1 =
                new ArrayList<Integer>(Arrays.asList(10, 20, 30, 40, 50));

        int target = 70;

        for (int i = 0; i < a1.size(); i++) {

            for (int j = i + 1; j < a1.size(); j++) {

                if (a1.get(i) + a1.get(j) == target) {

                    System.out.println("Elements : "
                            + a1.get(i) + " + " + a1.get(j));

                    System.out.println("Target : " + target);

                    return;
                }
            }
        }

        System.out.println("Two Sum Not Found");
    }
}
```

### Sample Output

```text
Elements : 20 + 50
Target : 70
```

````
````markdown
### Question 8

**Problem:**  
Write a Java program to find the **first positive missing number** in the range `1-10` using an `ArrayList`.

**Input:**  
ArrayList: `1, 2, 3, 4, 6, 7, 8, 9, 10`

### Java Code

```java
import java.util.ArrayList;
import java.util.Arrays;

public class P8 {
    public static void main(String[] args) {

        ArrayList<Integer> a1 =
                new ArrayList<Integer>(
                        Arrays.asList(1, 2, 3, 4, 6, 7, 8, 9, 10)
                );

        int n = a1.get(a1.size() - 1);

        int totalSum = n * (n + 1) / 2;

        int sum = 0;

        for (int i = 0; i < a1.size(); i++) {

            sum += a1.get(i);
        }

        System.out.println("Missing number is: " + (totalSum - sum));
    }
}
```

### Sample Output

```text
Missing number is: 5
```
