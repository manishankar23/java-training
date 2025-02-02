# PATTERN PROGRAMS IN JAVA
Pattern programs in Java are a popular way to practice logic building and enhance problem-solving skills. These programs generate visual representations of various patterns using characters, numbers, or symbols, such as stars (*). Patterns are created by leveraging loops and conditional statements, making them an excellent exercise for mastering the core concepts of programming.

The foundation of pattern creation lies in understanding the relationships between rows and columns, which are managed using nested loops. The outer loop generally controls the rows, while the inner loop handles the content within each row. Additionally, incorporating spaces strategically is crucial for formatting symmetrical patterns like pyramids or diamonds.

Java supports various types of pattern programs, ranging from simple star patterns to complex combinations. Star patterns include triangles, diamonds, and hollow shapes. Numeric patterns feature sequences, pyramids, or grids of numbers, while alphabet patterns utilize characters like A, B, C to create shapes.

Basic operations in pattern programs include using for loops for iteration, if-else conditions for specific rules, and string concatenation for formatting output. Advanced techniques, such as manipulating spaces or combining multiple elements, add complexity to the patterns. For example, a diamond pattern may require both increasing and decreasing sequences, along with precise alignment.

Practicing pattern programs builds strong logical thinking and mastery over loops, conditions, and basic input-output operations. These skills are critical for tackling coding challenges and are frequently tested in technical interviews. Moreover, they provide a deeper understanding of how code interacts with the console to produce structured output.

By exploring pattern programs, you gain hands-on experience with Java’s fundamentals while also developing the ability to analyze and solve problems systematically. This makes pattern programs a cornerstone of beginner programming exercises and a stepping stone to more advanced Java concepts.



# 1. Print Square or Rectangle of Stars
````[JAVA]
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int m = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= m; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
OUTPUT
5 5
* * * * *  
* * * * *  
* * * * *  
* * * * *  
* * * * *
````
# 2. Print Right-Angled Triangle of Stars
````
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
Input:
5

Output:
*  
* *  
* * *  
* * * *  
* * * * *
````

# 3. Print Hollow Square
````[JAVA]
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n; j++) {
                if (i == 1 || i == n || j == 1 || j == n) {
                    System.out.print("* ");
                } else {
                    System.out.print("  ");
                }
            }
            System.out.println();
        }
    }
}
Input:
5
* * * * *  
*       *  
*       *  
*       *  
* * * * *
````


### 4. Print Right-Aligned Triangle of Stars
````[JAVA]
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int sp = 1; sp <= n - i; sp++) {
                System.out.print(" ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
Input:
5
    *  
   * *  
  * * *  
 * * * *  
* * * * *
````
Here’s the continuation of structured titles, code, and output for the remaining programs:

---

### 5. **Print Right-Aligned Triangle without Spaces Between Stars**
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int sp = 1; sp <= n - i; sp++) {
                System.out.print(" ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
    *  
   **  
  ***  
 ****  
*****
```

---

### 6. **Print Right-Aligned Rectangle**
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int sp = 1; sp <= n - i; sp++) {
                System.out.print(" ");
            }
            for (int j = 1; j <= n; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
    * * * * *  
   * * * * *  
  * * * * *  
 * * * * *  
* * * * *
```

---

### 7. **Reverse Right-Aligned Triangle**
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = n; i >= 1; i--) {
            for (int sp = 1; sp <= n - i; sp++) {
                System.out.print("  ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
* * * * *  
  * * * *  
    * * *  
      * *  
        *  
```

---

### 8. **Reverse Right-Aligned Triangle without Double Spaces**
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = n; i >= 1; i--) {
            for (int sp = 1; sp <= n - i; sp++) {
                System.out.print(" ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
* * * * *  
 * * * *  
  * * *  
   * *  
    *
```

---

### 9. **Diamond Pattern**
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int sp = 1; sp <= n - i; sp++) {
                System.out.print("  ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
        for (int i = n - 1; i >= 1; i--) {
            for (int sp = 1; sp <= n - i; sp++) {
                System.out.print("  ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
        *  
      * *  
    * * *  
  * * * *  
* * * * *  
  * * * *  
    * * *  
      * *  
        *  
```

---

### 10. **Triangle Pattern with Increasing and Decreasing Rows**
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
        for (int i = n - 1; i >= 1; i--) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
*  
* *  
* * *  
* * * *  
* * * * *  
* * * *  
* * *  
* *  
*  
```

---

### 11. **Diamond with Spaces**
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int sp = 1; sp <= n - i; sp++) {
                System.out.print(" ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
        for (int i = n - 1; i >= 1; i--) {
            for (int sp = 1; sp <= n - i; sp++) {
                System.out.print(" ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
    *  
   * *  
  * * *  
 * * * *  
* * * * *  
 * * * *  
  * * *  
   * *  
    *  
```
Here’s the continuation of more structured pattern programs:

---

### 12. **Number Triangle (Ascending Numbers in Each Row)**  
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
1  
1 2  
1 2 3  
1 2 3 4  
1 2 3 4 5  
```

---

### 13. **Reverse Number Triangle (Descending Numbers in Each Row)**  
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = n; i >= 1; i--) {
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
1 2 3 4 5  
1 2 3 4  
1 2 3  
1 2  
1  
```

---

### 14. **Pyramid with Numbers**  
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int sp = 1; sp <= n - i; sp++) {
                System.out.print("  ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }
            for (int j = i - 1; j >= 1; j--) {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
        1  
      1 2 1  
    1 2 3 2 1  
  1 2 3 4 3 2 1  
1 2 3 4 5 4 3 2 1  
```

---

### 15. **Diamond with Numbers**  
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int sp = 1; sp <= n - i; sp++) {
                System.out.print(" ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }
            System.out.println();
        }
        for (int i = n - 1; i >= 1; i--) {
            for (int sp = 1; sp <= n - i; sp++) {
                System.out.print(" ");
            }
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
    1  
   1 2  
  1 2 3  
 1 2 3 4  
1 2 3 4 5  
 1 2 3 4  
  1 2 3  
   1 2  
    1  
```

---

### 16. **Floyd's Triangle**  
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int num = 1;
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(num + " ");
                num++;
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
1  
2 3  
4 5 6  
7 8 9 10  
11 12 13 14 15  
```

---

### 17. **Binary Triangle (Alternating 1s and 0s)**  
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print((i + j) % 2 + " ");
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
1  
0 1  
1 0 1  
0 1 0 1  
1 0 1 0 1  
```

---

### 18. **Hollow Square**  
**Code**:
```java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n; j++) {
                if (i == 1 || i == n || j == 1 || j == n) {
                    System.out.print("* ");
                } else {
                    System.out.print("  ");
                }
            }
            System.out.println();
        }
    }
}
```

**Input**:  
5  

**Output**:  
```
* * * * *  
*       *  
*       *  
*       *  
* * * * *  
```
