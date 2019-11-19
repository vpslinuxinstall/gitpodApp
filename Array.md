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

{% github_embed "https://github.com/peterlulu666/hackerrankTutorial/blob/master/src/Array/Main.java" %}{% endgithub_embed %}      


















        




        

