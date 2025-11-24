# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:

area(int side) for square

area(int length, int breadth) for rectangle

area(double radius) for circle

## AIM:
To write a Java program that calculates the area of different shapes using method overloading by defining multiple area() methods with different parameter lists for square, rectangle, and circle.

## ALGORITHM :
Start the program.

Create a class AreaCalculator.

Overload three methods named area():

area(int side) → calculates area of a square.

area(int length, int breadth) → calculates area of a rectangle.

area(double radius) → calculates area of a circle.

Create a main class and inside main() create an object of AreaCalculator.

Call each overloaded method with appropriate parameters.

Display the calculated areas.

End the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```java
class AreaCalculator {

    double area(int side) {
        return side * side;
    }

    double area(int length, int breadth) {
        return length * breadth;
    }
    double area(double radius) {
        return 3.14159 * radius * radius;
    }
}

public class Main {
    public static void main(String[] args) {

        AreaCalculator obj = new AreaCalculator();

        System.out.println("Area of Square: " + obj.area(5));
        System.out.println("Area of Rectangle: " + obj.area(10, 20));
        System.out.println("Area of Circle: " + obj.area(7.5));
    }
}

```
## OUTPUT:
<img width="1209" height="403" alt="Screenshot 2025-11-24 130829" src="https://github.com/user-attachments/assets/bd93f7e1-b67c-4757-9640-80421784c207" />


## RESULT:
Thus the program was successfully executed and the output was verified.
