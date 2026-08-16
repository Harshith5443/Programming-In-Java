````markdown
### Question 1

**Problem:**  
Write a Java program to sort the given **unsorted array into ascending order** using `Arrays.sort()`.

**Input:** `40, 10, 50, 20, 30`

### Java Code

```java
import java.util.Arrays;

public class P1 {
    public static void main(String[] args) {

        int[] arr = {40, 10, 50, 20, 30};

        Arrays.sort(arr);

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
Write a Java program to check whether the given number is **present in an array or not** and print its index.

**Input:**  
Array: `10, 20, 30, 40, 50`  
Search: `30`

### Java Code

```java
public class P2 {
    public static void main(String[] args) {

        int[] arr = {10, 20, 30, 40, 50};

        int search = 30;

        for (int i = 0; i < arr.length; i++) {

            if (arr[i] == search) {

                System.out.println("Number is Present index : " + i);

                return;
            }
        }

        System.out.println("Number is Not Present");
    }
}
```

### Sample Output

```text
Number is Present index : 2
```
````
````markdown
### Question 3

**Problem:**  
Write a Java program to find the **target value by adding two elements of an array**.

**Input:**  
Array: `10, 20, 30, 40, 50`  
Target: `70`

### Java Code

```java
public class P3 {
    public static void main(String[] args) {

        int[] arr = {10, 20, 30, 40, 50};

        int target = 70;

        for (int i = 0; i < arr.length; i++) {

            for (int j = i + 1; j < arr.length; j++) {

                if (arr[i] + arr[j] == target) {

                    System.out.println("Elements : " + arr[i] + " + " + arr[j]);
                    System.out.println("Target : " + target);

                    return;
                }
            }
        }

        System.out.println("Target Not Found");
    }
}
```

### Sample Output

```text
Elements : 20 + 50
Target : 70
```
