# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:

## AIM:
To write a Java program that demonstrates inheritance by creating a superclass Person and subclass Student, and to calculate a student's grade based on marks.

## ALGORITHM :
Start the program.

Create a superclass Person with fields name and age.

Create a subclass Student that extends Person.

Add an integer field marks in Student.

Create a constructor in Student to initialize name, age, and marks.

Implement method calculateGrade():

If marks ≥ 90 → Grade A

If marks ≥ 75 → Grade B

If marks ≥ 50 → Grade C

Else → Grade D

Create object of Student class in main method.

Print student details and calculated grade.

End the program.

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```java
class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

class Student extends Person {
    int marks;

    Student(String name, int age, int marks) {
        super(name, age);
        this.marks = marks;
    }

    public String calculateGrade() {
        if (marks >= 90)
            return "A";
        else if (marks >= 75)
            return "B";
        else if (marks >= 50)
            return "C";
        else
            return "D";
    }
}

public class Main {
    public static void main(String[] args) {
        Student s = new Student("John", 20, 88);

        System.out.println("Name: " + s.name);
        System.out.println("Age: " + s.age);
        System.out.println("Marks: " + s.marks);
        System.out.println("Grade: " + s.calculateGrade());
    }
}

```

## OUTPUT:
<img width="1018" height="546" alt="Screenshot 2025-11-24 130410" src="https://github.com/user-attachments/assets/ff4c611a-be28-4b94-be19-dd6988336779" />


## RESULT:
Thus the program was successfully executed and the output was verified.
