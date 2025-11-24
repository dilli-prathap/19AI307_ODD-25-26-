# Ex.No:2(B) METHODS

## QUESTION:
Write a method int square(int number) that returns the square of a given number.

## AIM:
To write a method square(int number) that takes a number as input and returns its square.

## ALGORITHM :

Start

Create a method square(int number)

Multiply number × number

Return the result

End

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```java
public class SquareDemo {

    // method to return square
    int square(int number) {
        return number * number;
    }

    public static void main(String[] args) {
        SquareDemo obj = new SquareDemo();
        int result = obj.square(5);  // example
        System.out.println("Square: " + result);
    }
}

```
## OUTPUT:
<img width="1816" height="937" alt="Screenshot 2025-11-24 124220" src="https://github.com/user-attachments/assets/cea94400-c2c3-4e43-831e-ce1a79f13b4c" />

## RESULT:
The method square(int number) successfully returns the square of the given number.
