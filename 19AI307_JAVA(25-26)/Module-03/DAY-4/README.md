# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.
 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

## AIM:

To write a Java program where two bots (SunBot and RainBot) implement a common interface to analyze weather data and give predictions based on the temperature.

## ALGORITHM :

Start

Create an interface WeatherBot with a method predict(int temperature)

Create SunBot class that implements WeatherBot:

If temperature > 30 → return "HOT"

Else → return "MODERATE"

Create RainBot class that implements WeatherBot:

If temperature < 20 → return "COLD"

Else → return "WARM"

In main():

Take temperature and botType (1 or 2)

If botType is 1 → create SunBot

If botType is 2 → create RainBot

Call predict() and print the output

End


## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```JAVA
import java.util.Scanner;

// Interface
interface WeatherBot {
    String predict(int temperature);
}

// SunBot class
class SunBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature > 30)
            return "HOT";
        else
            return "MODERATE";
    }
}

// RainBot class
class RainBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature < 20)
            return "COLD";
        else
            return "WARM";
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot;

        if (botType == 1)
            bot = new SunBot();
        else
            bot = new RainBot();

        System.out.println(bot.predict(temperature));
    }
}

```
## OUTPUT:
<img width="1586" height="458" alt="Screenshot 2025-11-24 222659" src="https://github.com/user-attachments/assets/7fbb9625-9bf3-4c32-a7f1-1143b24ce9d9" />

## RESULT:
THUS THE PROGRAM WAS EXECUTED SUCCESSFULLY AND THE OUTPUT WAS VERIFIED .
