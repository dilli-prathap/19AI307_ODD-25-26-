# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:

Write a Java program to simulate inter-thread communication using PipedInputStream and PipedOutputStream, where one thread writes data (input taken from the user) and another thread reads and displays the data.

## AIM:

To write a Java program that demonstrates inter-thread communication using PipedInputStream and PipedOutputStream, where one thread sends user-entered data through a pipe and another thread receives and prints that data.

## ALGORITHM :

1. Read user input.

2. Create `PipedOutputStream` and connect to `PipedInputStream`.

3. Create and start WriterThread to write data to the pipe.

4. Create and start ReaderThread to read data from the pipe.

5. WriterThread writes bytes and closes stream.

6. ReaderThread reads bytes, converts to string, and prints.

7. End.

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```java 
import java.io.*;
import java.util.Scanner;

class WriterThread extends Thread {
    private PipedOutputStream pos;
    private String message;

    public WriterThread(PipedOutputStream pos, String message) {
        this.pos = pos;
        this.message = message;
    }

    @Override
    public void run() {
        try {
            pos.write(message.getBytes());
            pos.close();
        } catch (IOException e) {
            System.out.println("WriterThread Error: " + e.getMessage());
        }
    }
}

class ReaderThread extends Thread {
    private PipedInputStream pis;

    public ReaderThread(PipedInputStream pis) {
        this.pis = pis;
    }

    @Override
    public void run() {
        try {
            byte[] buffer = new byte[1024];
            int bytesRead = pis.read(buffer);

            if (bytesRead != -1) {
                String received = new String(buffer, 0, bytesRead);
                System.out.println("ReaderThread received: " + received);
            }

            pis.close();
        } catch (IOException e) {
            System.out.println("ReaderThread Error: " + e.getMessage());
        }
    }
}

public class PipedStreamUserInputDemo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        try {
            
            String userMessage = scanner.nextLine();

           
            PipedOutputStream pos = new PipedOutputStream();
            PipedInputStream pis = new PipedInputStream(pos);

           
            WriterThread writer = new WriterThread(pos, userMessage);
            ReaderThread reader = new ReaderThread(pis);

            reader.start();
            writer.start();

        } catch (IOException e) {
            System.out.println("Main Error: " + e.getMessage());
        } finally {
            scanner.close();
        }
    }
}
```

## OUTPUT:
<img width="1254" height="399" alt="517675939-f0811c9c-6e8c-4652-ac8a-7850f36b1b1f" src="https://github.com/user-attachments/assets/f0966ab1-f7b2-4fee-a0bb-c5856ca78d95" />


## RESULT:

The program transfers user input from one thread to another using piped streams and displays the received message.
