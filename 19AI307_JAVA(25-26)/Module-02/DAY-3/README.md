# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## AIM:
To write a Java program that creates a class Smartphone with private variables brand, model, and storageCapacity, along with public getter and setter methods. The program should also include a method increaseStorage() that increases the storage by a given value.

## ALGORITHM :
Start the program.

Create a class Smartphone with private instance variables:

brand (String)

model (String)

storageCapacity (int)

Create public getter and setter methods for all variables.

Create a method increaseStorage(int value) that adds the value to the current storage.

Create a display() method to print smartphone details.

In the main class:

Take user input for brand, model, storage capacity, and additional storage.

Call setters to assign values.

Call increaseStorage().

Display updated details.

End the program.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: DILLI PRATHAP 
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```JAVA
import java.util.Scanner;

class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    // Getters
    public String getBrand() {
        return brand;
    }
    public String getModel() {
        return model;
    }
    public int getStorageCapacity() {
        return storageCapacity;
    }

    // Setters
    public void setBrand(String brand) {
        this.brand = brand;
    }
    public void setModel(String model) {
        this.model = model;
    }
    public void setStorageCapacity(int storageCapacity) {
        this.storageCapacity = storageCapacity;
    }

    // Increase storage
    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }

    // Display details
    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Smartphone sp = new Smartphone();

        // Inputs
        String brand = sc.nextLine();
        String model = sc.nextLine();
        int storage = sc.nextInt();
        int increase = sc.nextInt();

        // Setting values
        sp.setBrand(brand);
        sp.setModel(model);
        sp.setStorageCapacity(storage);

        // Increase storage
        sp.increaseStorage(increase);

        // Display updated details
        sp.display();
    }
}

```
## OUTPUT:

<img width="1768" height="688" alt="Screenshot 2025-11-24 215922" src="https://github.com/user-attachments/assets/8622842f-eecc-4dbe-ab4d-c7884ed244bf" />


## RESULT:

THUS THE PROGRAM WAS EXECUTED SUCCESSFULLY AND THE OUTPUT WAS VERIFIED .
