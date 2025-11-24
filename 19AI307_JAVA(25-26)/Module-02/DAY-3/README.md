# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## AIM:
To create a Java class Smartphone with private variables brand, model, and storageCapacity, provide getter/setter methods, and implement increaseStorage() to add extra storage. The program should read input, update storage, and display updated details.

## ALGORITHM :
Start the program.

Create a class Smartphone with private variables.

Write public getters and setters for each variable.

Write increaseStorage(int value) to add the given value to storageCapacity.

Write display() to print smartphone details.

In main(),

Take brand, model, storage, and value to increase.

Set values using setters.

Call increaseStorage(value).

Call display().

End.




## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    public String getBrand() { return brand; }
    public String getModel() { return model; }
    public int getStorageCapacity() { return storageCapacity; }

    public void setBrand(String brand) { this.brand = brand; }
    public void setModel(String model) { this.model = model; }
    public void setStorageCapacity(int storageCapacity) { this.storageCapacity = storageCapacity; }

    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }

    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String brand = sc.next();
        String model = sc.next();
        int storage = sc.nextInt();
        int increase = sc.nextInt();

        Smartphone phone = new Smartphone();
        phone.setBrand(brand);
        phone.setModel(model);
        phone.setStorageCapacity(storage);

        phone.increaseStorage(increase);
        phone.display();
    }
}

```
## OUTPUT:
<img width="1377" height="494" alt="Screenshot 2025-11-24 124807" src="https://github.com/user-attachments/assets/90486aaa-3c63-41f7-be22-65cb5e63fd0f" />

## RESULT:
Thus the program was executed successfully and the output was verified.

