# Interface
import java.util.Scanner;
// Define the Calculator interface
interface Calculator {
double add(double a, double b);
double subtract(double a, double b);
double multiply(double a, double b);
double divide(double a, double b);
}
// Implement the interface in SimpleCalculator
class SimpleCalculator implements Calculator {
@Override
public double add(double a, double b) {
return a + b;
}
@Override
public double subtract(double a, double b) {
return a - b;
}
@Override
public double multiply(double a, double b) {
return a * b;
}
@Override
public double divide(double a, double b) {
if (b == 0) {
System.out.println("Error: Division by zero is not allowed!");
return Double.NaN; // Return &quot;Not a Number&quot; if division by zero
}
return a / b;
}
}
// Main class to test the program
public class CalculatorProgram {
public static void main(String[] args) {
Scanner scanner = new Scanner(System.in);
Calculator calculator = new SimpleCalculator();
System.out.println("Welcome to the Simple Calculator!");
// Input two numbers
System.out.print("Enter the first number: ");
double num1 = scanner.nextDouble();
System.out.print("Enter the second number: ");
double num2 = scanner.nextDouble();
// Perform calculations

System.out.println("\nResults:");
System.out.println("Addition: " + calculator.add(num1, num2));
System.out.println("Subtraction: " + calculator.subtract(num1, num2));
System.out.println("Multiplication: " + calculator.multiply(num1, num2));
System.out.println("Division: " + calculator.divide(num1, num2));
scanner.close();
}
}
OUTPUT:
Welcome to the Simple Calculator!
Enter the first number: 56.12
Enter the second number: 12.11

Results:
Addition: 68.22999999999999
Subtraction: 44.01
Multiplication: 679.6131999999999
Division: 4.634186622625929
BUILD SUCCESSFUL (total time: 37 seconds)

