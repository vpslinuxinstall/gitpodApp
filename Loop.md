# Loop      

## For loop      

```java      
int endOfRange = 4;
for(int i = 0; i < endOfRange; i++){
    System.out.println(i);
}     

```      

## While loop     

```java     
int min = 0;
int max = 4;
while(true){
    System.out.println(min++);      
    if (min >= max){
        break;       

    }
}      

```      

## Problem      

{% urlembed %}
assets/A2.pdf
{% endurlembed %}      


## Programming      

```java        

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int number;      
        while (true){
            number = scanner.nextInt();
            if (number <= 20 && number >= 2){
                break;
                
            }

        }
        scanner.close();
        for (int i = 1; i <= 10; i++) {
            System.out.println(number + " x " + i + " = " + number * i);

        }

    }
}        

```        









































