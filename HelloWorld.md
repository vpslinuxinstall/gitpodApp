# Class      

The class is a collection of variables and functions. The program is a collection of classes.      

We would write the class name in CamelCase.      

# Variable        

## Naming convention in Java for variables        

We would write variable name in lowercase letter. When the name has more than one words we would use camelCase. Lower snake case is used frequently in C, C++ and Python, but it is not the naming convention in Java.                          

## Data type        

We would declare a variable like this `DataType myVariable`.        

We would declare and initialize a variable like this `DataType myVar1 = value`.       

## Function      

A sequence of packaged instructions that perform a task.      

## Method      

It is the same as function.        

## Object       

It is the instance of a class.        

## Stream        

IO input and output.      

User input.      

Print to console.        

```java      
Scanner scan = new Scanner(System.in); // open scanner
String s = scan.next(); // read the next token and save it to 's'
scan.close(); // close scanner
System.out.println(s); // print 's' to System.out, followed by a new line      

```      

                     



## Problem      

{% urlembed %}
assets/A1.pdf
{% endurlembed %}      


## Programming      

```java      
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;
public class Solution {
    public static void main(String[] args) {
        // Create a Scanner object to read input from stdin.
        Scanner scan = new Scanner(System.in); 
        
        // Read a full line of input from stdin and save it to our variable, inputString.
        String inputString = scan.nextLine(); 

        // Close the scanner object, because we've finished reading 
        // all of the input from stdin needed for this challenge.
        scan.close(); 
      
        // Print a string literal saying "Hello, World." to stdout.
        System.out.println("Hello, World.");
        
      
        // TODO: Write a line of code here that prints the contents of inputString to stdout.
        System.out.println(inputString);        
        
             
    }
}        

```      
















