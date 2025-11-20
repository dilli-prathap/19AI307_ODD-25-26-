# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a Java program to reverse a given string.

## AIM:

To reverse a given string.

## ALGORITHM :

1. **Start the program.**
2. Declare a variable to store the input string.
3. Read the string from the user.
4. Create an empty string variable `reversed` to store the final reversed string.
5. Use a loop that starts from the **last character** of the string and moves to the **first character**:

   * For each iteration, append the current character to `reversed`.
6. After the loop ends, `reversed` will contain the reversed string.
7. Print the reversed string.
8. **End the program.**

---


## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

class ReverseString {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String str = sc.nextLine();

        String reversed = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            reversed = reversed + str.charAt(i);
        }

        System.out.println("Reversed string: " + reversed);

        sc.close();
    }
}
```

## OUTPUT:

<img width="1629" height="579" alt="Screenshot 2025-11-20 225223" src="https://github.com/user-attachments/assets/24bac92c-1723-4f20-9c4c-305d34a09545" />

## RESULT:

Thus the program was executed successfully and the output was verified.
