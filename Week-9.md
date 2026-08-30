````markdown
### Question 1

**Problem:**  
Write a Java program to sort the given array using **Bubble Sort**.

**Input:** `40, 10, 50, 20, 30`

### Java Code

```java
import java.util.Arrays;

public class P1 {
    public static void main(String[] args) {

        int[] arr = {40, 10, 50, 20, 30};

        for (int i = 0; i < arr.length - 1; i++) {

            for (int j = 0; j < arr.length - 1 - i; j++) {

                if (arr[j] > arr[j + 1]) {

                    int temp = arr[j];

                    arr[j] = arr[j + 1];

                    arr[j + 1] = temp;
                }
            }
        }

        // Arrays.toString() is used to print the array
        System.out.println("Sorted Array : " + Arrays.toString(arr));
    }
}
```

### Sample Output

```text
Sorted Array : [10, 20, 30, 40, 50]
```
````
````markdown
### Question 2

**Problem:**  
Write a Java program to find the **first positive missing number** in the range `1-10`.

**Input:** `1, 2, 3, 4, 6, 7, 8, 9, 10`

### Java Code

```java
public class P2 {
    public static void main(String[] args) {

        int[] arr = {1, 2, 3, 4, 6, 7, 8, 9, 10};

        int n = arr[arr.length - 1];

        int totalSum = n * (n + 1) / 2;

        int sum = 0;

        for (int i = 0; i < arr.length; i++) {

            sum += arr[i];
        }

        System.out.println("Missing number is: " + (totalSum - sum));
    }
}
```

### Sample Output

```text
Missing number is: 5
```
````
````markdown
### Question 3

**Problem:**  
Write a Java program to **rotate the array towards the right direction based on the key value**.

**Input:**  
Array: `1, 2, 3, 4, 5`  
Key: `10`

### Java Code

```java
import java.util.Arrays;

public class P3 {
    public static void main(String[] args) {

        int[] arr = {1, 2, 3, 4, 5,6};

        int key = 10;

        int n = arr.length;

        int k = key % n;

        int[] temp = new int[n];

        for (int i = 0; i < n; i++) {

            temp[(i + k) % n] = arr[i];
            // (index + rotationValue) % lengthOfArray
        }

        System.out.println("Right Rotated Array : " + Arrays.toString(temp));
    }
}
```
### Sample Output

```text
Right Rotated Array : [3, 4, 5, 6, 1, 2]
```

````
````markdown
### Question 4

**Problem:**  
Write a Java program to **rotate the array towards the left direction based on the key value**.

**Input:**  
Array: `1, 2, 3, 4, 5, 6`  
Key: `10`

### Java Code

```java
import java.util.Arrays;

public class P4 {
    public static void main(String[] args) {

        int[] arr = {1, 2, 3, 4, 5, 6};

        int key = 10;

        int n = arr.length;

        int k = key % n;

        int[] temp = new int[n];

        for (int i = 0; i < n; i++) {

            temp[i] = arr[(i + k) % n];
            // (index + rotationValue) % lengthOfArray
        }

        System.out.println("Left Rotated Array : " + Arrays.toString(temp));
    }
}
```

### Sample Output

```text
Left Rotated Array : [5, 6, 1, 2, 3, 4]
```
````
````markdown
### Question 5

**Problem:**  
Write a Java program to print the **zero values first and later the other numbers**.

**Input:**  
Array: `1, 0, 0, 2, 3, 0, 4`

### Java Code

```java
import java.util.Arrays;

public class P5 {
    public static void main(String[] args) {

        int[] arr = {1, 0, 0, 2, 3, 0, 4};

        int[] temp = new int[arr.length];

        int index = 0;

        for (int i = 0; i < arr.length; i++) {

            if (arr[i] == 0) {

                temp[index] = arr[i];

                index++;
            }
        }

        for (int i = 0; i < arr.length; i++) {

            if (arr[i] != 0) {

                temp[index] = arr[i];

                index++;
            }
        }

        System.out.println("Zero First Array : " + Arrays.toString(temp));
    }
}
```

### Sample Output

```text
Zero First Array : [0, 0, 0, 1, 2, 3, 4]
```

````
````markdown
### Question 6

**Problem:**  
Write a Java program to print the **non-zero numbers first and zero values last**.

**Input:**  
Array: `1, 0, 0, 2, 3, 0, 4`

### Java Code

```java
public class Main {
    public static void main(String[] args) {

        int[] arr = {1, 0, 0, 2, 3, 0, 4};
        int[] temp=new int[arr.length];
        int index=0;

        // Print non-zero numbers first
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] != 0) {
                temp[index]=arr[i];
                index++;
            }
        }
        System.out.println("Zero First Array : " + Arrays.toString(temp));
    }
}
```

### Sample Output

```text
1 2 3 4 0 0 0
```
````
````markdown
### Question 7

**Problem:**  
Write a Java program to print the **positive numbers first and negative numbers last**.

**Input:**  
Array: `-1, 1, 3, -2, 4, 0, -5`

### Java Code

```java
public class Main {
    public static void main(String[] args) {

        int[] arr = {-1, 1, 3, -2, 4, 0, -5};
        int [] temp=new int[arr.length];
        int index=0;

        // Print positive numbers first
        for (int i = 0; i < arr.length; i++) {

            if (arr[i] >= 0) {
               temp[index]=arr[i];
                index++;
            }
        }

        // Print negative numbers last
        for (int i = 0; i < arr.length; i++) {

            if (arr[i] < 0) {
                temp[index]=arr[i];
                index++;
            }
        }
        System.out.println("Zero First Array : " + Arrays.toString(temp));
    }
}
```

### Sample Output

```text
1 3 4 -1 -2 -5
```
