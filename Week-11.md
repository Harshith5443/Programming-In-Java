````markdown

## Question 1

**Problem:**  
Write a Java program to search for an element in a sorted array using binary search.

### Java Code

```java
import java.util.Arrays;

public class P1 {
    public static void main(String[] args) {

        int[] arr = {10, 20, 30, 40, 50};
        int search = 30;

        int low = 0;
        int high = arr.length - 1;

        while (low <= high) {

            int mid = (low + high) / 2;

            if (arr[mid] == search) {
                System.out.println("Element Found at index : " + mid);
                return;
            } else if (arr[mid] < search) {
                low = mid + 1;
            } else {
                high = mid - 1;
            }
        }

        System.out.println("Element Not Found");
    }
}
