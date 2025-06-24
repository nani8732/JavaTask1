#The program is a simple console-based calculator written in Java. It supports:

Addition

Subtraction

Multiplication

Division

The program runs in a loop, allowing the user to perform multiple calculations until they choose to exit.

🔍 Code Explanation
1. Importing Scanner
java
Copy
Edit
import java.util.Scanner;
Imports the Scanner class for reading user input from the console.

2. Calculator Class
java
Copy
Edit
public class Calculator {
The main class that contains all methods and logic for the calculator.

3. Arithmetic Methods
java
Copy
Edit
public static double add(double a, double b) { return a + b; }
public static double subtract(double a, double b) { return a - b; }
public static double multiply(double a, double b) { return a * b; }
public static double divide(double a, double b) {
    if (b == 0) {
        System.out.println("Error: Division by zero!");
        return 0;
    }
    return a / b;
}
These static methods perform the basic arithmetic operations.

divide() handles division by zero to avoid a runtime error.

4. Main Method
java
Copy
Edit
public static void main(String[] args) {
The entry point of the program.

5. Initialize Scanner and Loop Flag
java
Copy
Edit
Scanner scanner = new Scanner(System.in);
boolean continueCalc = true;
Scanner is used for taking user input.

continueCalc controls the loop for repeated calculations.

6. Welcome Message
java
Copy
Edit
System.out.println("Welcome to Java Console Calculator!");
7. Main Loop
java
Copy
Edit
while (continueCalc) {
    ...
}
This loop runs continuously until the user chooses to exit.

8. Operation Menu
java
Copy
Edit
System.out.println("1. Addition");
System.out.println("2. Subtraction");
System.out.println("3. Multiplication");
System.out.println("4. Division");
System.out.println("5. Exit");
Displays the available operations to the user.

9. User Choice Input
java
Copy
Edit
int choice = scanner.nextInt();
Reads the operation choice from the user.

10. Exit Condition
java
Copy
Edit
if (choice == 5) {
    System.out.println("Exiting calculator. Goodbye!");
    break;
}
Ends the loop if the user selects option 5.

11. Input Two Numbers
java
Copy
Edit
System.out.print("Enter first number: ");
double num1 = scanner.nextDouble();
System.out.print("Enter second number: ");
double num2 = scanner.nextDouble();
Takes two numbers from the user for the operation.

12. Perform Operation Using switch-case
java
Copy
Edit
switch (choice) {
    case 1: result = add(num1, num2); break;
    case 2: result = subtract(num1, num2); break;
    case 3: result = multiply(num1, num2); break;
    case 4: result = divide(num1, num2); break;
    default: 
        System.out.println("Invalid choice! Please select a number from 1 to 5.");
        continue;
}
Depending on the user's choice, it calls the appropriate method.

If the choice is invalid, it continues the loop.

13. Display Result
java
Copy
Edit
System.out.println("Result: " + result);
14. Close Scanner
java
Copy
Edit
scanner.close();
Releases the resources once the loop is done (although it's outside the loop, so it only runs once at the end).

