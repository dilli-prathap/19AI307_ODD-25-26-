# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
You are designing a microservices-based system where multiple services like AuthService, UserService, OrderService, etc., need to log important system events.

## AIM:
To design a microservices system where multiple services can log important events consistently using a common logging mechanism.

## ALGORITHM :

Start

Read number of log entries n

For each entry:

Read service, level, and message
Get Logger instance
Add the log
Print current logs
End



## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```java
import java.util.*;

class Logger {
    private static Logger instance = null;
    private List<String> logs;

    private Logger() {
        logs = new ArrayList<>();
    }

    public static Logger getInstance() {
        if (instance == null) {
            instance = new Logger();
        }
        return instance;
    }

    
    public void addLog(String service, String level, String message) {
        String logMessage = service + " " + level + ": " + message;
        logs.add(logMessage);

        System.out.println(logMessage);
        System.out.println("Current Logs:");
        for (int i = 0; i < logs.size(); i++) {
            System.out.println((i + 1) + ". " + logs.get(i));
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); 
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String[] input = sc.nextLine().split(" ");
            String service = input[0];
            String level = input[1];
            String message = input[2];

            Logger logger = Logger.getInstance();
            logger.addLog(service, level, message);
            System.out.println();
        }
        sc.close();
    }
}
```
## OUTPUT:

<img width="1221" height="849" alt="517673830-a084d57c-dfd1-49bd-aa25-25a02f3ab012" src="https://github.com/user-attachments/assets/35c1053e-a897-49f5-8720-f9cc2ef1acb3" />



## RESULT:

The program ensures all services use a single Logger instance, records each log entry, and displays the complete log history after every new entry.
