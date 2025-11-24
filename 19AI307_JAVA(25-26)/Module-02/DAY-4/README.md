# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to access a static variable using both class name and object.

## AIM:
To access a static variable using both class name and object.


## ALGORITHM :
Start the program.

Create a class called Demo.

Inside the class, declare a static variable (e.g., count).

In the main method:

Access the static variable using the class name.

Create an object of Demo.

Access the same static variable using the object reference.

Print both values.

End the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```JAVA
class Demo {
    static int count = 10; 
}

public class StaticExample {
    public static void main(String[] args) {
        System.out.println("Using class name: " + Demo.count);

        Demo obj = new Demo();
        System.out.println("Using object: " + obj.count);
    }
}

```
## OUTPUT:
<img width="1138" height="407" alt="Screenshot 2025-11-24 125419" src="https://github.com/user-attachments/assets/1290c68e-b66e-4fcc-95d9-689951318bc5" />

## RESULT:
Thus the program was successfully executed and the output was verified.
