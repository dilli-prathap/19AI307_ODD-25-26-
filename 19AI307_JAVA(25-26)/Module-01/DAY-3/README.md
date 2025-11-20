# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.

## AIM:

To write a Java program that calculates the factorial of a given number using a **for loop**, where the factorial of a number *n* is the product of all positive integers from 1 to *n*.

---

## ALGORITHM :

1. **Start the program.**
2. Declare a variable to store the number (n).
3. Read the value of n from the user.
4. Initialize a variable `fact` to **1** (since factorial multiplication starts from 1).
5. Use a **for loop** from 1 to n:

   * Multiply `fact` by the loop counter each time.
6. After the loop ends, the variable `fact` will hold the factorial of n.
7. Print the value of `fact`.
8. **End the program.**

---

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: DILLI PRATHAP 
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

class FactorialProgram {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = sc.nextInt();

        int fact = 1;

        for (int i = 1; i <= n; i++) {
            fact = fact * i;
        }

        System.out.println("Factorial of " + n + " is: " + fact);

        sc.close();
    }
}
```

## OUTPUT:

<img width="1561" height="545" alt="Screenshot 2025-11-20 224223" src="https://github.com/user-attachments/assets/28e3f5a9-47db-4c12-ab7a-1d86c708ab45" />


## RESULT:
Thus the program was executed successfully and the result was verified .
