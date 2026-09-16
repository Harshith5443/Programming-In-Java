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

```
````
````markdown
## Question 2

**Problem:**  
Write a Java program to group anagrams from a given array of strings.

### Java Code

```java
import java.util.Arrays;
import java.util.HashMap;
import java.util.ArrayList;

public class P2 {
    public static void main(String[] args) {

        String[] arr = {"eat", "tea", "tan", "ate", "nat", "bat"};

        HashMap<String, ArrayList<String>> map = new HashMap<>();

        for (String word : arr) {

            char[] ch = word.toCharArray();

            Arrays.sort(ch);

            String key = new String(ch);

            map.putIfAbsent(key, new ArrayList<>());

            map.get(key).add(word);
        }

        System.out.println(map.values());
    }
}

```
````
````markdown
## Question 2

**Problem:**  
Write a Java program to find the maximum amount of water that can be stored between two vertical lines.

### Java Code

```java
public class P2 {
    public static void main(String[] args) {

        int[] arr = {1, 8, 6, 2, 5, 4, 8, 3, 7};

        int i = 0;
        int j = arr.length - 1;
        int maxWater = 0;

        while (i < j) {

            int height = Math.min(arr[i], arr[j]);
            int width = j - i;

            int water = height * width;

            if (water > maxWater) {
                maxWater = water;
            }

            if (arr[i] < arr[j]) {
                i++;
            } else {
                j--;
            }
        }

        System.out.println("Maximum Water : " + maxWater);
    }
}
