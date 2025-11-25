# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## AIM:
write a Java program that reads two integers from the user, performs division, and handles the ArithmeticException if the second number is zero.

## ALGORITHM :

Start the program.

Read two integers: num1 and num2.

Use a try–catch block to perform the division.

In the try block:

Calculate result = num1 / num2.

Print the result.

In the catch block (ArithmeticException):

Print "Error: Division by zero".

End the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```JAVA
import java.util.Scanner;

class DivisionProgram {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        try {
            int result = a / b;
            System.out.println("Result: " + result);
        } catch (ArithmeticException e) {
            System.out.println("Error: Division by zero");
        }
    }
}

```
## OUTPUT:
<img width="939" height="360" alt="Screenshot 2025-11-25 183954" src="https://github.com/user-attachments/assets/c5ee8923-6e9c-489e-b62e-a4b8cc634f60" />



## RESULT:
THUS THE PROGRAM WAS EXECUTED SUCCESSFULLY AND THE OUTPUT WAS VERIFIED.
