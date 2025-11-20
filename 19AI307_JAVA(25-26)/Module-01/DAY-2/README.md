# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:

In a magical building, an elevator behaves oddly:

If the floor number is divisible by 3 and 5, it says "Skipped".

If the floor number is divisible by 3 only, it says "Beware!".

If the floor number is divisible by 5 only, it says "Blessings!".

Otherwise, it announces the floor number - print - "Floor {number}" .

Write a Java program to simulate this elevator logic for a given floor number.

## AIM:

To write a Java program that simulates a magical elevator’s behavior based on the floor number.
The program should check whether the given floor number is divisible by 3, 5, or both, and display specific messages:

* If divisible by **both 3 and 5**, print **"Skipped"**
* If divisible by **3 only**, print **"Beware!"**
* If divisible by **5 only**, print **"Blessings!"**
* Otherwise, print **"Floor {number}"**

---

## ALGORITHM :

1. **Start the program.**
2. Declare a variable to store the floor number.
3. Read the floor number from the user.
4. Check if the floor number is **divisible by both 3 and 5**:

   * If true, print **"Skipped"**.
5. Else, check if the floor number is **divisible by 3 only**:

   * If true, print **"Beware!"**.
6. Else, check if the floor number is **divisible by 5 only**:

   * If true, print **"Blessings!"**.
7. Else:

   * Print **"Floor {number}"**.
8. **End the program.**

---


## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: DILLI PRATHAP
RegisterNumber: 212224110014
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

class ElevatorMagic {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the floor number: ");
        int floor = sc.nextInt();

        if (floor % 3 == 0 && floor % 5 == 0) {
            System.out.println("Skipped");
        } else if (floor % 3 == 0) {
            System.out.println("Beware!");
        } else if (floor % 5 == 0) {
            System.out.println("Blessings!");
        } else {
            System.out.println("Floor " + floor);
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="1645" height="618" alt="Screenshot 2025-11-20 223636" src="https://github.com/user-attachments/assets/f0bfc327-e4a0-4c0a-8797-cc908c42d464" />


## RESULT:
Thus the program was executed successfully and verified.
