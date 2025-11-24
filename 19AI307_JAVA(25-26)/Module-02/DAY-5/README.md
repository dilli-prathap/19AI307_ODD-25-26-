# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".


## AIM:
The program should access the static method using the class name and the non-static method using an object.

## ALGORITHM :
Start the program.

Create a class Calculator.

Inside the class, define a non-static method add(int a, int b) that returns the sum.

Define a static method info() that prints "Calculator is ready".

In the main() method (class prog):

Call the static method using Calculator.info().

Create an object of Calculator.

Call the non-static method add(a, b) using the object.

Print the result.

End the program.




## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Calculator {

    // Non-static method
    int add(int a, int b) {
        return a + b;
    }

    // Static method
    static void info() {
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {
        Calculator.info();

        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt();
        int y = sc.nextInt();
        Calculator obj = new Calculator();
        int result = obj.add(x, y);

        System.out.println("Sum: " + result);
    }
}

```
## OUTPUT:
<img width="1839" height="665" alt="Screenshot 2025-11-24 125756" src="https://github.com/user-attachments/assets/d989434a-17fd-48ea-8cbc-be617ab7bfcf" />


## RESULT:
Thus the program was successfully executed and the output was verified.
