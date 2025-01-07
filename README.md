import java.util.*;
public class Hello{
    public static void main(String[] args){
        System.out.println("Harsha Chary V");
    }
}

import java.util.Scanner;
import java.util.Random;
import java.util.Arrays;

public class SimpleJavaPrograms {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        // -------------------- Simple Output ---------------------
        System.out.println("------ Simple Output ------");
        System.out.println("Hello, Java!");
        System.out.println("This is a simple Java program.");


        // -------------------- Variable Declaration and Usage --------------------
        System.out.println("\n------ Variables ------");
        int age = 30;
        double price = 19.99;
        String name = "Alice";

        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Price: $" + price);


        // -------------------- Basic Arithmetic --------------------
        System.out.println("\n------ Arithmetic ------");
        int num1 = 10;
        int num2 = 5;

        int sum = num1 + num2;
        int difference = num1 - num2;
        int product = num1 * num2;
        int quotient = num1 / num2;
        int remainder = num1 % num2;

        System.out.println("Sum: " + sum);
        System.out.println("Difference: " + difference);
        System.out.println("Product: " + product);
        System.out.println("Quotient: " + quotient);
        System.out.println("Remainder: " + remainder);

        // -------------------- User Input --------------------
        System.out.println("\n------ User Input ------");
        System.out.print("Enter your name: ");
        String userName = scanner.nextLine();
        System.out.println("Hello, " + userName + "!");

        System.out.print("Enter your age: ");
        int userAge = scanner.nextInt();
        System.out.println("You are " + userAge + " years old.");
        scanner.nextLine(); // Consume the newline character after nextInt()

        // -------------------- Conditional Statements (if-else) --------------------
        System.out.println("\n------ Conditional Statements ------");
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();

        if (number > 0) {
            System.out.println("The number is positive.");
        } else if (number < 0) {
            System.out.println("The number is negative.");
        } else {
            System.out.println("The number is zero.");
        }
        scanner.nextLine(); // Consume the newline

        // -------------------- Switch Statement --------------------
         System.out.println("\n------ Switch Statement ------");
         System.out.print("Enter a day (1-7): ");
         int day = scanner.nextInt();
         String dayName;
         switch(day){
              case 1: dayName = "Sunday";
                      break;
              case 2: dayName = "Monday";
                      break;
              case 3: dayName = "Tuesday";
                      break;
              case 4: dayName = "Wednesday";
                      break;
              case 5: dayName = "Thursday";
                      break;
              case 6: dayName = "Friday";
                      break;
              case 7: dayName = "Saturday";
                      break;
              default: dayName = "Invalid day";
                      break;
          }
         System.out.println("It is "+ dayName);

         scanner.nextLine();


        // -------------------- Loops (for loop) --------------------
        System.out.println("\n------ For Loop ------");
        System.out.println("Counting from 1 to 5:");
        for (int i = 1; i <= 5; i++) {
            System.out.print(i + " ");
        }
        System.out.println();

        // -------------------- Loops (while loop) --------------------
        System.out.println("\n------ While Loop ------");
        int counter = 1;
        while (counter <= 5) {
            System.out.println("Counter: " + counter);
            counter++;
        }

       // -------------------- Loops (do-while loop) --------------------
        System.out.println("\n------ Do-While Loop ------");
        int doCounter = 5;
        do{
           System.out.println("Do-While Counter: "+ doCounter);
           doCounter--;
        } while(doCounter > 0);

        // -------------------- Arrays --------------------
        System.out.println("\n------ Arrays ------");
        int[] numbers = {10, 20, 30, 40, 50};
        System.out.println("Array Elements:");
        for (int i = 0; i < numbers.length; i++) {
            System.out.print(numbers[i] + " ");
        }
        System.out.println();


        // -------------------- Array Manipulation --------------------
        System.out.println("\n------ Array Manipulation ------");
        System.out.print("Enter size of array: ");
        int arraySize = scanner.nextInt();
        int[] dynamicArray = new int[arraySize];

        for (int i = 0; i < arraySize; i++){
           System.out.print("Enter array element " + (i+1) + ": ");
           dynamicArray[i] = scanner.nextInt();
        }
         System.out.println("Your array is: " + Arrays.toString(dynamicArray));
         Arrays.sort(dynamicArray);
         System.out.println("Your sorted array is: " + Arrays.toString(dynamicArray));
        scanner.nextLine();



         // -------------------- Random Number Generation --------------------
         System.out.println("\n------ Random Number Generation ------");
         int randomNumber = random.nextInt(100); // Generate random num between 0-99
         System.out.println("Random number: " + randomNumber);

          // -------------------- String Manipulation --------------------
         System.out.println("\n------ String Manipulation ------");
         System.out.print("Enter a String: ");
         String inputString = scanner.nextLine();
         System.out.println("String length: "+ inputString.length());
         System.out.println("String to Uppercase: " + inputString.toUpperCase());
         System.out.println("String to Lowercase: " + inputString.toLowerCase());
         System.out.println("First character: " + inputString.charAt(0));
          if (inputString.contains("Java"))
          {
               System.out.println("String contains 'Java'");
          } else {
              System.out.println("String does not contain 'Java'");
          }


         // -------------------- Simple Method Call --------------------
        System.out.println("\n------ Method call ------");
        int squareResult = calculateSquare(5);
        System.out.println("Square of 5: " + squareResult);


        // -------------------- Method Overloading --------------------
        System.out.println("\n------ Method Overloading ------");
        System.out.println("Sum of 2 integers: " + addNumbers(10,20));
        System.out.println("Sum of 3 integers: " + addNumbers(10, 20, 30));
        System.out.println("Sum of 2 doubles: " + addNumbers(10.5, 20.5));

        // -------------------- Exception Handling (try-catch) --------------------
        System.out.println("\n------ Exception Handling ------");
        try {
          System.out.print("Enter a number to divide 10 by: ");
          int divisor = scanner.nextInt();
          int result = 10 / divisor;
          System.out.println("Result of division is: " + result);

        } catch(ArithmeticException e){
          System.out.println("Error: Cannot divide by zero!");
        }  catch (java.util.InputMismatchException e){
            System.out.println("Error: Please enter a valid integer!");
        } finally {
              System.out.println("Finally block always executed");
              scanner.nextLine(); //Consume the left out newline
        }
        scanner.close();


    }

    // Simple method for calculating square
    public static int calculateSquare(int number){
      return number * number;
    }
    // Method Overloading examples
    public static int addNumbers(int num1, int num2){
        return num1+num2;
    }
    public static int addNumbers(int num1, int num2, int num3){
        return num1+num2+num3;
    }
    public static double addNumbers(double num1, double num2){
        return num1+num2;
    }
}

