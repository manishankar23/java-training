## JAVA BASIC PROGRAMS
### EVEN AND ODD
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        for (int i = 1; i <= n; i++) {
            if (i % 2 == 0) {
                System.out.println(+i);
            }
        }
        for (int i = 1; i <= n; i++) {
            if (i % 2 != 0) {
                System.out.println(+i);
            }
        }
    }
}
```
**Input:**  
5

**Output:**  
2  
4  
1  
3  
5  

---

### FACTORIAL
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        int fact = 1;
        for (int i = 2; i <= n; i++) {
            fact = fact * i;
        }
        System.out.print(fact);
    }
}
```
**Input:**  
5

**Output:**  
120

---

### MULTIPLICATION TABLE
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        for (int i = 1; i <= 10; i++) {
            System.out.println(i + "X" + n + "=" + i * n);
        }
    }
}
```
**Input:**  
5

**Output:**  
1X5=5  
2X5=10  
3X5=15  
4X5=20  
5X5=25  
6X5=30  
7X5=35  
8X5=40  
9X5=45  
10X5=50

---

### REVERSE OF A NUMBER
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        int s1 = 0, rev = 1;
        while (n > 0) {
            rev = n % 10;
            s1 = s1 * 10 + rev;
            n = n / 10;
        }
        System.out.print(s1);
    }
}
```
**Input:**  
12345

**Output:**  
54321

---

### COUNT DIGITS IN A NUMBER
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        int count = 0;
        while (n > 0) {
            n = n / 10;
            count++;
        }
        System.out.print(count);
    }
}
```
**Input:**  
12345

**Output:**  
5

---

### SUM OF EVEN NUMBERS
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        int sum = 0;
        for (int i = 1; i <= n; i++) {
            if (i % 2 == 0) {
                System.out.println(+i);
                sum += i;
            }
        }
        System.out.println(sum);
    }
}
```
**Input:**  
5

**Output:**  
2  
4  
6

---

### PALINDROME NUMBER
```java
import java.util.*;
public class Main
{
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(n);
        int s1 = 0, rev = 1;
        int temp = n;
        while (n > 0) {
            rev = n % 10;
            s1 = s1 * 10 + rev;
            n = n / 10;
        }
        System.out.print(s1);
        if (s1 == temp) {
            System.out.println("PALINDROME");
        }
    }
}
```
**Input:**  
121

**Output:**  
121  
PALINDROME
