
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
