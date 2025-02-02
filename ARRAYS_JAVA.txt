## ARRAY PROGRAMS IN JAVA
  Arrays in Java are one of the fundamental data structures that allow storing multiple values of the same type in a single variable. An array in Java is a container object that holds a fixed number of values of a single type. Arrays are indexed, starting from 0, and their size is defined at the time of declaration. Java arrays are objects, and they come with several advantages, such as easy access to elements via their indices and efficient storage.

  The core operations with arrays include initialization, traversal, and manipulation of elements. Arrays can be statically or dynamically initialized, and Java offers several methods for array manipulation. For example, you can find the maximum or minimum values in an array, sort the array in ascending or descending order, and search for specific elements. Searching and sorting algorithms, like linear search, binary search, and bubble sort, are often implemented to work with arrays.

  Handling duplicates in arrays is also a common task, and Java provides simple techniques to remove or identify duplicates. Another frequent operation involves merging arrays or combining the contents of multiple arrays into one. Arrays in Java can be multidimensional, allowing the storage of data in matrix form, which is useful in complex problems like image processing or scientific computations.

  Although Java arrays have a fixed size, they provide efficient memory usage and fast access to elements. For scenarios requiring frequent changes in the array size or modifications to its content, the ArrayList class (which belongs to the java.util package) can be a more flexible alternative. Arrays are a powerful tool for developers, widely used in algorithms, data manipulation, and application development.Mastering array operations in Java is essential for working with data efficiently, whether it's sorting, searching, merging, or handling complex structures.

### **1. Find Maximum and Minimum Element in an Array**
#### Code:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        int a[] = {1, 11, 22, 3, 2, 5, 6, 10, 8};

        int max = 0;
        int min = a[0];

        for (int i = 1; i < a.length; i++) {
            if (max < a[i]) {
                max = a[i];
            }
            if (min > a[i]) {
                min = a[i];
            }
        }
        System.out.println(max);
        System.out.println(min);
    }
}
```
#### Input:
No input required; array is predefined.

#### Output:
```
22
1
```

---

### **2. Check if an Element is Present in the Array**
#### Code:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a[] = new int[5];
        boolean found = false;

        for (int i = 0; i < a.length; i++) {
            a[i] = s.nextInt();
        }
        int target = s.nextInt();

        for (int i = 1; i < a.length; i++) { 
            if (a[i] == target) {
                found = true;
            }
        }
        System.out.println(found);
    }
}
```
#### Input:
```
1 2 3 4 5
3
```

#### Output:
```
true
```

---

### **3. Sort Array in Ascending Order**
#### Code:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a[] = new int[5];

        for (int i = 0; i < a.length; i++) {
            a[i] = s.nextInt();
        }

        for (int i = 0; i < a.length; i++) {
            for (int j = 0; j < a.length; j++) {
                if (a[i] < a[j]) {
                    int temp = a[i];
                    a[i] = a[j];
                    a[j] = temp;
                }
            }
        }

        for (int i = 0; i < a.length; i++) {
            System.out.println(a[i]);
        }
    }
}
```
#### Input:
```
4 2 5 1 3
```

#### Output:
```
1
2
3
4
5
```

---

### **4. Find the Second Largest Element in an Array**
#### Code:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a[] = new int[5];

        for (int i = 0; i < a.length; i++) {
            a[i] = s.nextInt();
        }

        for (int i = 0; i < a.length; i++) {
            for (int j = 0; j < a.length; j++) {
                if (a[i] < a[j]) {
                    int temp = a[i];
                    a[i] = a[j];
                    a[j] = temp;
                }
            }
        }
        System.out.println(a[a.length - 2]);
    }
}
```
#### Input:
```
4 2 5 1 3
```

#### Output:
```
4
```

---

### **5. Remove Duplicates (Adjacent Only)**
#### Code:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a[] = new int[5];

        for (int i = 0; i < a.length; i++) {
            a[i] = s.nextInt();
        }

        for (int i = 0; i < a.length - 1; i++) {
            if (a[i] == a[i + 1]) {
                System.out.println(a[i]);
            }
        }
    }
}
```
#### Input:
```
1 1 2 3 3
```

#### Output:
```
1
3
```

---

### **6. Merge Two Arrays**
#### Code:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a[] = new int[5];
        int b[] = new int[5];
        int c[] = new int[10];

        for (int i = 0; i < a.length; i++) {
            a[i] = s.nextInt();
        }
        for (int i = 0; i < b.length; i++) {
            b[i] = s.nextInt();
        }

        for (int i = 0; i < a.length; i++) {
            c[i] = a[i];
        }

        for (int i = 0; i < b.length; i++) {
            c[a.length + i] = b[i];
        }

        System.out.println(Arrays.toString(c));
    }
}
```
#### Input:
```
1 2 3 4 5
6 7 8 9 10
```

#### Output:
```
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

---

### **7. Remove Duplicates (Results Only Once)**
#### Code:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a[] = new int[5];

        for (int i = 0; i < a.length; i++) {
            a[i] = s.nextInt();
        }

        for (int i = 0; i < a.length; i++) {
            if (i == 0 || a[i] != a[i - 1]) {
                System.out.println(a[i]);
            }
        }
    }
}
```
#### Input:
```
1 2 2 3 3
```

#### Output:
```
1
2
3
```

