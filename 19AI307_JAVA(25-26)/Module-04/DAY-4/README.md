# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create a program that loads an operating system shell using the Factory Pattern. Based on user input, return a shell object: windows, linux, mac.

## AIM:
To develop a program that uses the Factory Pattern to create and return the appropriate operating system shell (Windows, Linux, or Mac) based on user input.

## ALGORITHM :

1. Start

2. Read the operating system name from the user

3. Call `ShellFactory.getShell(osName)` to get the corresponding shell object

4. If the returned shell is `null`:
   * Print “Invalid OS”

5. Else:
   * Call `startShell()` on the shell object

6. End
## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

interface Shell {
    void startShell();
}

class WindowsShell implements Shell {
    public void startShell() {
        System.out.println("Loading Windows shell...");
    }
}

class LinuxShell implements Shell {
    public void startShell() {
        System.out.println("Loading Linux shell...");
    }
}

class MacShell implements Shell {
    public void startShell() {
        System.out.println("Loading Mac shell...");
    }
}

class ShellFactory {
    public static Shell getShell(String osName) {
        if (osName == null) return null;
        switch (osName.toLowerCase()) {
            case "linux":
                return new LinuxShell();
            case "mac":
                return new MacShell();
            case "windows":
                return new WindowsShell();
            default:
                return null;
        }
    }
}

public class FactoryShellDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();
        Shell shell = ShellFactory.getShell(input);
        if (shell == null) {
            System.out.println("Invalid OS: " + input);
        } else {
            shell.startShell();
        }
        sc.close();
    }
}

```
## OUTPUT:
<img width="797" height="518" alt="517674444-ce753850-7d3e-4b2c-9e5f-eae49e29d049" src="https://github.com/user-attachments/assets/511e48ee-37f1-4de6-8f8d-142d72148bbe" />



## RESULT:
The program selects the correct OS shell using the Factory Pattern and loads it, or displays an error if the OS name is invalid.
