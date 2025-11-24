# Ex.No:3(E) INNER CLASS

## QUESTION:
 Write a Java program where the inner class is declared private and accessed through a method in the outer class. 

## AIM:
To write a Java program that demonstrates private inner class access using a public method of the outer class. The outer class stores a value inside a private inner class and prints it using the outer class's method.

## ALGORITHM :

tart the program.

Create an Outer class.

Inside it, declare a private inner class named Inner.

Give the private inner class a variable to store the value.

Add a method inside Outer that:

Creates an object of the private inner class.

Sets the value.

Prints the value.

In main(), take input from the user.

Call the method of outer class to access and print data from the inner class.

End the program.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```JAVA
import java.util.Scanner;

class Outer {

    // Private Inner Class
    private class Inner {
        int data;

        Inner(int data) {
            this.data = data;
        }

        void show() {
            System.out.println("Data set inside private inner class: " + data);
        }
    }

    // Method to access private inner class
    public void accessInner(int value) {
        Inner obj = new Inner(value);
        obj.show();
    }
}

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        Outer outer = new Outer();
        outer.accessInner(n);
    }
}

```
## OUTPUT:
<img width="1773" height="878" alt="Screenshot 2025-11-24 223254" src="https://github.com/user-attachments/assets/30fdcc73-1fee-47e7-a9db-d6b3342c3c87" />


## RESULT:
THUS THE PROGRAM WAS EXECUTED SUCCESSFULLY AND THE OUTPUT WAS VERIFIED .
