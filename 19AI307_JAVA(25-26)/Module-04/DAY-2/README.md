# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a gaming lounge, there is only one master console power switch that controls all gaming consoles. Whenever a player turns on any console, it internally triggers the master power. The master switch must ensure only one instance is ever created, regardless of how many times it's accessed, to prevent power fluctuations.

Every time a player accesses the master switch, it logs an access count. Since the switch is Singleton, the count should increment globally and reflect shared state.

## AIM:
To develop a Java program that implements the Singleton Design Pattern for a master power switch in a gaming lounge. The master switch should always return the same instance and maintain a globally shared access counter, regardless of how many players attempt to access it.

## ALGORITHM :
Start the program.

Create a class MasterSwitch.

Declare a private static instance of MasterSwitch (initially null).

Make the constructor private so no external object can be created.

Add a static method getInstance():

If instance is null → create new MasterSwitch

Otherwise return the existing instance

Add a variable accessCount, initially 0.

Each time getInstance() is called, increment accessCount.

Create a main class and simulate multiple players accessing the master switch.

Print the access count after each access to verify shared behavior.

End the program.
## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014 
*/
```

## SOURCE CODE:
```JAVA
import java.util.*;

class MasterPowerSwitch {
    private static MasterPowerSwitch instance = null;
    private int accessCount = 0; // shared counter

    // Private constructor
    private MasterPowerSwitch() {}

    // Singleton Instance Access
    public static MasterPowerSwitch getInstance() {
        if (instance == null) {
            instance = new MasterPowerSwitch();
        }
        return instance;
    }

    // Method to log each access
    public void accessSwitch(String playerName) {
        accessCount++;
        System.out.println(playerName + " accessed Master Power Switch. Total accesses so far: " + accessCount);
    }
}

public class MainProgram {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        MasterPowerSwitch mps = MasterPowerSwitch.getInstance();

        for (int i = 0; i < n; i++) {
            String name = sc.next();
            mps.accessSwitch(name);
        }
    }
}
```
## OUTPUT:
<img width="1605" height="407" alt="Screenshot 2025-11-25 184411" src="https://github.com/user-attachments/assets/d9612e28-6211-47bf-93ea-ff1b3287f430" />



## RESULT:
THUS THE PROGRAM WAS EXECUTED SUCCESSFULLY AND THE OUTPUT WAS VERIFIED.
