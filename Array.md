# Array              

## Data structure      

Data storage, retrieval, and use.      

## Array      

A type of data structure that store same type data.      

### Print array        







```java      
package test;

import java.util.Arrays;

public class Main {
    // Generic type array
    public static <E> void prinArray(E[] arr) {
        System.out.print("[");
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i]);
            if (i < arr.length - 1) {
                System.out.print(", ");
            }

        }
        System.out.println("]");

    }

    // Integer type array
    public static void prinArrayInt(Integer[] arr) {
        System.out.print("[");
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i]);
            if (i < arr.length - 1) {
                System.out.print(", ");
            }

        }
        System.out.println("]");

    }

    // String type array
    public static void prinArrayStr(String[] arr) {
        System.out.print("[");
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i]);
            if (i < arr.length - 1) {
                System.out.print(", ");
            }

        }
        System.out.println("]");

    }

    public static void main(String[] args) {
        // Declare array
        Integer[] arr0 = new Integer[3];
        // Declare and initialize integer array
        Integer[] arr = {1, 2, 3};
        // Print array
        System.out.println(Arrays.toString(arr));
        prinArray(arr);
        prinArrayInt(arr);
        // Declare and initialize string array
        String[] shoppingList = {"bananas", "apples", "pears"};
        // Print array
        System.out.println(Arrays.toString(shoppingList));
        prinArray(shoppingList);
        prinArrayStr(shoppingList);

    }
}        

```       

## Problem      

{% urlembed %}
assets/A3.pdf
{% endurlembed %}        

## Programming        

```java      
package Array;

import java.util.Arrays;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
//        System.out.println("Enter array size ");
        // Read size through scanner.nextLine()
        String sizeStr = scanner.nextLine();
        // String size to int size
        int size = Integer.parseInt(sizeStr);
        // We would use scanner.nextInt() to read size like this
        // We would add scanner.nextLine() after scanner.nextInt() to consume rest of that line including newline, so the following nextLine() will work fine
//        int size = scanner.nextInt();
//        scanner.nextLine();
//        System.out.println("Enter array and use space to separate integer ");
        String arrStr = scanner.nextLine();
        String[] arrStrSplit = arrStr.split(" ");
        scanner.close();
        int[] numberArr = new int[size];
        for (int i = 0; i < size; i++) {
            numberArr[i] = Integer.parseInt(arrStrSplit[i]);

        }

        // Print array in reverse order
//        System.out.print("[");
        for (int i = numberArr.length - 1; i >= 0; i--) {
            System.out.print(numberArr[i]);
            if (i >= 1) {
                System.out.print(", ");

            }

        }
//        System.out.print("]");

        // Print array in reverse order
//        int[] reversedNumberArr = new int[size];
//        int count = size;
//        for (int i = 0; i < size; i++) {
//            reversedNumberArr[count - 1] = numberArr[i];
//            count--;
//
//        }
//        for (int i = 0; i < size; i++) {
//            System.out.print(reversedNumberArr[i]);
//            if (i < size - 1) {
//                System.out.print(" ");
//
//            }
//
//        }
//
    }
}        

```        














        




        

