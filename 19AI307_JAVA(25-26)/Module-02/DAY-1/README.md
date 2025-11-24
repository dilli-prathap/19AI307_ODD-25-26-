# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## AIM:
To write a Java program that defines a class Car with attributes brand, model, and year, creates two objects of the class, and prints their details to the console.

## ALGORITHM :
1.	Start the program.
2. Create a class named **Car** and import packages.
3. Inside the class, declare three variables:

   * **brand** (String)
   * **model** (String)
   * **year** (int)
4. Write a **constructor** to initialize these attributes.
5. Create another class (e.g., **CarMain**) with the **main()** method.
6. Inside the main method:

   * Create **object 1** of Car with values (e.g., "Toyota", "Innova", 2022).
   * Create **object 2** of Car with values (e.g., "Hyundai", "i20", 2021).
7. Print the details of both Car objects in the given format.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Dilli Prathap 
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```java
class Car {
    String brand;
    String model;
    int year;

    // Constructor
    Car(String brand, String model, int year) {
        this.brand = brand;
        this.model = model;
        this.year = year;
    }
}

public class CarMain {
    public static void main(String[] args) {

        // Creating 2 Car objects
        Car car1 = new Car("Toyota", "Innova", 2022);
        Car car2 = new Car("Hyundai", "i20", 2021);

        // Printing details
        System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
        System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
    }
}

```
## OUTPUT:
<img width="1697" height="645" alt="Screenshot 2025-11-24 121211" src="https://github.com/user-attachments/assets/8756a03f-9963-4ea5-b1fb-417e5e92a70e" />



## RESULT:
The program successfully created two Car objects and displayed their details:

Car 1 is a Toyota Innova manufactured in 2022.

Car 2 is a Hyundai i20 manufactured in 2021.
