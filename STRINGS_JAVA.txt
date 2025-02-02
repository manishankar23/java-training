# PLACEMENT_TRAINING-JAVA
Strings in Java are one of the most fundamental and widely used data types, representing a sequence of characters. They are immutable, meaning once a String object is created, its content cannot be changed. This immutability ensures security, thread safety, and efficient memory handling. Strings are defined using the String class, and Java provides rich functionality for string manipulation.
Basic operations include concatenation using + or the concat() method, finding the length of a string using length(), and accessing individual characters with charAt(). String case conversions, such as toUpperCase() and toLowerCase(), are frequently used for formatting. Methods like trim() help in removing leading and trailing whitespaces, while substring() extracts parts of a string based on specified indices.
Advanced operations enable robust string handling. Reversing a string, counting specific characters, and replacing words with replace() or replaceAll() are common in solving real-world problems. Regular expression support enhances flexibility, allowing pattern matching and validation with methods like matches().
Java also supports mutable alternatives to strings, such as StringBuilder and StringBuffer, for scenarios requiring frequent modifications. Whether working with text processing, data parsing, or application development, mastering string operations is essential for efficient Java programming. This versatility makes strings a cornerstone in both beginner and advanced programming tasks.

# Concatenation in Java
```[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        String s2 = "Dharu";
        System.out.println("Print the statement: " + s1 + " " + s2);
    }
}
OUTPUT
Print the statement: Hello Dharu
````

# Finding Length in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        int length = s1.length();
        System.out.println("Print the statement: " + length);
    }
}
OUTPUT
Print the statement: 5
````


# charAt() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        char ch = s1.charAt(3);
        System.out.println("Print the statement: " + ch);
    }
}
OUTPUT
Print the statement: l
````

# Uppercase Conversion
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        System.out.println("Print the statement: " + s1.toUpperCase());
    }
}
OUTPUT
Print the statement: HELLO
````

# Lowercase Conversion
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        System.out.println("Print the statement: " + s1.toLowerCase());
    }
}
OUTPUT
Print the statement: hello
````

# indexOf() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        System.out.println("Print the statement: " + s1.indexOf('e'));
    }
}
OUTPUT
Print the statement: 1
````

# lastIndexOf() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        System.out.println("Print the statement: " + s1.lastIndexOf('o'));
    }
}
OUTPUT
Print the statement: 4
````

# startsWith() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello DHARUU";
        System.out.println("Print the statement: " + s1.startsWith("Hello"));
    }
}
OUTPUT
Print the statement: true
````

# endsWith() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello DHARUU";
        System.out.println("Print the statement: " + s1.endsWith("Hello"));
    }
}
OUTPUT
Print the statement: false
````

# Substring
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello DHARUU";
        System.out.println("Print the statement: " + s1.substring(3));
    }
}
OUTPUT
Print the statement: lo DHARUU
````


# Replace All
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello Dee";
        System.out.println("Print the statement: " + s1.replaceAll("el", "ae"));
    }
}
OUTPUT
Print the statement: Haelo Dee
````

# Trim in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "  Hello World  ";
        System.out.println("Print the statement: " + s1.trim());
    }
}
OUTPUT
Print the statement: Hello World
````

# Split in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello World";
        String[] words = s1.split(" ");
        System.out.println("Print the statement: " + words[0] + " " + words[1]);
    }
}
OUTPUT
Print the statement: Hello World
````


# valueOf() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        int num = 123;
        String s1 = String.valueOf(num);
        System.out.println("Print the statement: " + s1);
    }
}
OUTPUT
Print the statement: 123
````

# matches() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello World";
        System.out.println("Print the statement: " +s1.matches(".*World.*"));
    }
}
OUTPUT
Print the statement: true
````


# replaceFirst() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello World World";
        System.out.println("Print the statement: " + s1.replaceFirst("World", "Dharu"));
    }
}
OUTPUT
Print the statement: Hello Dharu World
````



# isEmpty() in Java
````[JAVA]
public class Main {
    public static void main(String[] args) {
        String s1 = "";
        System.out.println("Print the statement: " + s1.isEmpty());
    }
}
OUTPUT
Print the statement: true
````


# toCharArray() in Java
````
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello";
        char[] chars = s1.toCharArray();
        System.out.println("Print the statement: " + chars[0] + chars[1] + chars[2] + chars[3] + chars[4]);
    }
}
OUTPUT
Print the statement: Hello
````

# equals() in Java
````
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello World";
        String s2 = "Hello World";
        System.out.println("Print the statement: " + s1.equals(s2));
    }
}
OUTPUT
Print the statement: true
````

# equalsIgnoreCase() in Java
````
public class Main {
    public static void main(String[] args) {
        String s1 = "hello world";
        String s2 = "Hello World";
        System.out.println("Print the statement: " + s1.equalsIgnoreCase(s2));
    }
}
OUTPUT
Print the statement: true
````


# IMPORTANT JAVA STRING PROBLEMS

# Reversing a String
````
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello Dee";
        String rev = "";
        for (int i = s1.length() - 1; i >= 0; i--) {
            rev += s1.charAt(i);
        }
        System.out.println("Print the statement: " + rev);
    }
}

OUTPUT
Print the statement: eeD olleH
````

# Occurrence of a Character in a String
````
public class Main {
    public static void main(String[] args) {
        String s1 = "Hello dharuu";
        char ch = 'l';
        int count = 0;
        for (int i = 0; i < s1.length(); i++) {
            if (s1.charAt(i) == ch) {
                count++;
            }
        }
        System.out.println("Print the statement: " + count);
    }
}
OUTPUT
Print the statement: 2
````


# Check if a String Contains Only Alphabetic Characters
````
public class Main {
    public static void main(String[] args) {
        String s1 = "HelloDharu";
        if(s1.matches("[a-zA-Z]+")){
            
        System.out.println(" TRUE");
    }
    else{
        System.out.println("FALSE");
    }
}
}
OUTPUT
 HelloDharu-TRUE
 HelloDharu21-FALSE
````

# MINI PROJECT ON STRINGS
# Question: Write a Java program that implements a simple login system. The system should prompt the user to input a username and password. If the entered credentials match a predefined username and password (Dharu93 and Dharu@90), it should display "Login Success". If the credentials don't match, it should display "Invalid Username or Password". The program should also use the following string methods:
# trim() - To remove any leading or trailing spaces from the entered credentials.
# equals() - To check if the entered username and password exactly match the predefined ones.
# equalsIgnoreCase() - To allow case-insensitive comparison of the credentials.
````
import java.util.*;
public class Main {
    public static void main(String[] args) {
        String u_name = "Dharu";
        String u_pw = "Dharuu90";
        Scanner s = new Scanner(System.in);
        String ip_name = s.next().trim(); 
        String ip_pw = s.next().trim();   
        System.out.println("Trimmed Username: " + ip_name);
        System.out.println("Trimmed Password: " + ip_pw);

        if (u_name.equals(ip_name) && u_pw.equals(ip_pw)) {
            System.out.println("Login Success");
        } else {
            System.out.println("Invalid Username or Password");
        }
    }
}
OUTPUT
1)           Dharu
Dharuu90     
Trimmed Username: Dharu
Trimmed Password: Dharuu90
Login Success
2) dHaruu
Dharuu98787
Trimmed Username: dHaruu
Trimmed Password: Dharuu98787
Invalid Username or Password

`````
# MINI PROJECT-2
# Question: Consider a simple text editor that allows you to find and replace words in a given text. You have an input sentence:
# "Java Basic Intro for 2 lines"
# Your task is to perform the following operations:
# Use the replace() method to replace every occurrence of the word "Java" with "Strings".
# Use the replaceAll() method to replace the phrase "Java Basic" with "Strings Basic".
# Use the matches() method to check if the word "Java" is present in the sentence. If it is present, print a message saying "Java is found in the text", otherwise print "Java is not found in the text".

````
import java.util.*;
public class Main {
    public static void main(String[] args) {
        String s = "Java is a programming language. Java is platform independent. Java is very easy.";
        
        System.out.println("INPUT TEXT:"  +s);
        String r_s = s.replace("Java", "Strings");
        System.out.println("THE REPLACED TEXT IS : " + r_s);

        String r_a = s.replaceAll("Java is", "Strings are");
        System.out.println("THE REPLACEDALL TEXT IS: " + r_a);
        if (s.matches(".*Java.*")) {
            System.out.println("TRUE,Java present in the text.");
        } else {
            System.out.println("Java not present in the text.");
        }
    }
}

OUTPUT
INPUT TEXT:Java is a programming language. Java is platform independent. Java is very easy.
THE REPLACED TEXT IS : Strings is a programming language. Strings is platform independent. Strings is very easy.
THE REPLACEDALL TEXT IS: Strings are a programming language. Strings are platform independent. Strings are very easy.
TRUE,Java present in the text.
````















