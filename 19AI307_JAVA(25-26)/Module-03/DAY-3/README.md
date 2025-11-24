# Ex.No:3(C) ABSTRACTION

## QUESTION:
Description:
Create abstract class GameScore with method finalScore().
Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

## AIM:
To implement an abstract class GameScore, extend it using subclasses ArcadeGame and PuzzleGame, and calculate the final score based on different game rules.

## ALGORITHM :
Create an abstract class GameScore with an abstract method finalScore().

Create subclass ArcadeGame with fields: baseScore, level.

Override finalScore() → return baseScore + (level × 100).

Create subclass PuzzleGame with field attempts.

Override finalScore():

If attempts ≤ 3 → return 1000 – attempts × 100

Else → return 500

In the main method, create objects of both classes and display final score.

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```java
abstract class GameScore {
    abstract int finalScore();
}

// ArcadeGame subclass
class ArcadeGame extends GameScore {
    private int baseScore;
    private int level;

    ArcadeGame(int baseScore, int level) {
        this.baseScore = baseScore;
        this.level = level;
    }

    @Override
    int finalScore() {
        return baseScore + (level * 100);
    }
}

// PuzzleGame subclass
class PuzzleGame extends GameScore {
    private int attempts;

    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }

    @Override
    int finalScore() {
        if (attempts <= 3) {
            return 1000 - (attempts * 100);
        } else {
            return 500;
        }
    }
}

// Main Program
public class GameMain {
    public static void main(String[] args) {

        ArcadeGame a1 = new ArcadeGame(500, 3);
        PuzzleGame p1 = new PuzzleGame(2);

        System.out.println("Arcade Game Final Score: " + a1.finalScore());
        System.out.println("Puzzle Game Final Score: " + p1.finalScore());
    }
}

```
## OUTPUT:

<img width="1701" height="582" alt="Screenshot 2025-11-24 222238" src="https://github.com/user-attachments/assets/ff051d52-d84c-4578-8a89-475fd04ca4bd" />


## RESULT:

THUS THE PROGRAM WAS EXECUTED SUCCESSFULLY AND THE OUTPUT WAS VERIFIED .
