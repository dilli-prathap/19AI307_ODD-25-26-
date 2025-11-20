# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to sort an array in ascending order.

## AIM:
To sort an array in ascending order.

## ALGORITHM :

1. **Start the program.**
2. Declare an array with a set of numbers.
3. Find the length of the array and store it in a variable `n`.
4. Use an outer loop from **i = 0 to n − 1**:

   * This selects each element one by one.
5. Inside the outer loop, use an inner loop from **j = i + 1 to n − 1**:

   * This compares the selected element with the remaining elements.
6. If **array[i] > array[j]**, then:

   * Swap `array[i]` and `array[j]`.
7. Continue the process until all elements are compared and swapped when necessary.
8. After the loops finish, the array is sorted in **ascending order**.
9. Print the sorted array.
10. **End the program.**

---

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: DILLI PRATHAP
RegisterNumber:  212224110014
*/
```

## SOURCE CODE:
```JAVA
import java.util.Scanner;

class SortArrayAscending {
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the number of elements: ");
        int n = sc.nextInt();

        int arr[] = new int[n];

        System.out.println("Enter " + n + " elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        // Sorting in ascending order
        for (int i = 0; i < n; i++) {
            for (int j = i + 1; j < n; j++) {
                if (arr[i] > arr[j]) {
                    // swap
                    int temp = arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
            }
        }

        System.out.println("Array sorted in ascending order:");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }

        sc.close();
    }
}

```
## OUTPUT:
<img width="1489" height="719" alt="Screenshot 2025-11-20 224709" src="https://github.com/user-attachments/assets/50394324-4f46-4592-9490-ebda176036c8" />



## RESULT:
Thus the program was executed successfully and the output was verified.
