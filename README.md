# Simple-Calculator
# Simple Calculator Application

## Description

A console-based Java program that performs basic arithmetic operations: addition, subtraction, multiplication, and division. It demonstrates fundamental Java concepts including methods and exception handling.

## Features

- **Addition**: Adds two integers.
- **Subtraction**: Subtracts the second integer from the first.
- **Multiplication**: Multiplies two integers.
- **Division**: Divides the first integer by the second, with error handling for division by zero.

## How to Run

1. **Clone the repository**:
    ```
    git clone https://github.com/yourusername/Calculator.git
    cd Calculator
    ```

2. **Compile the Java file**:
    ```
    javac src/Calculator.java
    ```

3. **Run the Java file**:
    ```
    java -cp src Calculator
    ```

## Example Code

```java
public class Calculator {
    public static void main(String[] args) {
        Calculator calc = new Calculator();
        System.out.println("Addition: " + calc.add(10, 5));
        System.out.println("Subtraction: " + calc.subtract(10, 5));
        System.out.println("Multiplication: " + calc.multiply(10, 5));
        System.out.println("Division: " + calc.divide(10, 5));
    }

    public int add(int a, int b) { return a + b; }
    public int subtract(int a, int b) { return a - b; }
    public int multiply(int a, int b) { return a * b; }
    public double divide(int a, int b) {
        if (b == 0) { throw new IllegalArgumentException("Division by zero is not allowed."); }
        return (double) a / b;
    }
}
