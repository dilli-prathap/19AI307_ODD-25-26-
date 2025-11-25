# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:

Use ScheduledExecutorService to delay execution of tasks and print their message.

## AIM:

To write a Java program that demonstrates the use of `ScheduledExecutorService` to schedule tasks with a delay and print their messages after the specified delay.

## ALGORITHM :

1. Read number of tasks `n`.

2. Create `ScheduledExecutorService` and `CountDownLatch(n)`.

3. For each task:

   * Read message and delay.
   * Schedule task to print message after delay and count down latch.

4. Wait for all tasks to finish.

5. Shutdown scheduler.

6. End.

## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```java
import java.util.concurrent.*;
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine());
        ScheduledExecutorService scheduler = Executors.newSingleThreadScheduledExecutor();
        CountDownLatch latch = new CountDownLatch(n);

        for (int i = 0; i < n; i++) {
            String line = sc.nextLine();
            int lastSpace = line.lastIndexOf(' ');
            String msg = line.substring(0, lastSpace);
            int delay = Integer.parseInt(line.substring(lastSpace + 1));
            scheduler.schedule(() -> {
                System.out.println(msg);
                latch.countDown();
            }, delay, TimeUnit.SECONDS);
        }

        try { latch.await(); } catch (InterruptedException e) {}

        scheduler.shutdown();
    }
}
```
## OUTPUT:

<img width="975" height="735" alt="517676674-ff591773-1d0c-4990-a6cf-bd833f7e667f" src="https://github.com/user-attachments/assets/71e5d4f8-1d75-436f-ad45-632484b7eeb7" />


## RESULT:
The program schedules tasks with specified delays using ScheduledExecutorService and prints each task’s message after its delay.


