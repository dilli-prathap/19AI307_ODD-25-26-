# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:
To write a Java program that checks whether a given number is an Armstrong number using Math.pow() and the Integer wrapper class, while taking input from the user.

## ALGORITHM :
Start the program.

Read a number from the user.

Convert the number to a string or use Integer.toString() to count its digits.

Extract each digit using % 10.

For each digit, compute digitⁿ using Math.pow(digit, numberOfDigits).

Add all powered digits.

Compare the sum with the original number:

If equal → Armstrong number

Else → Not an Armstrong number

Print the result.

End program.

## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

public class ArmstrongCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Taking input
        int num = sc.nextInt();
        int original = num;

        // Counting digits using Integer wrapper class
        int digits = Integer.toString(num).length();

        int sum = 0;

        // Calculating Armstrong sum
        while (num > 0) {
            int digit = num % 10;
            sum += (int)Math.pow(digit, digits);
            num /= 10;
        }

        // Checking Armstrong
        if (sum == original) {
            System.out.println(original + " is an Armstrong number");
        } else {
            System.out.println(original + " is NOT an Armstrong number");
        }
    }
}

```
## OUTPUT:

<img width="1761" height="717" alt="Screenshot 2025-11-24 223517" src="https://github.com/user-attachments/assets/c8c78e80-00a4-4484-9677-71556756de9f" />


## RESULT:
THUS THE PROGRAM WAS EXECUTED SUCCESSFULLY AND THE OUTPUT WAS VERIFIED .
