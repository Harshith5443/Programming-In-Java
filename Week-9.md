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
````markdown
````markdown
````markdown
````markdown
