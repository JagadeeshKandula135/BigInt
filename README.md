# BigInt Library

## Introduction

The BigInt library provides a way to handle very large integers in C++. By utilizing strings to store numbers as characters in reverse order, this library can efficiently manage, manipulate, and perform arithmetic operations on large integers beyond the limit of standard data types.

## Features

1. **Defining Big Integers**: Create and initialize large integer values.
2. **Digit Count**: Check the number of digits in a big integer.
3. **Increment/Decrement**: Perform pre/post incrementation and decrementation.
4. **Addition**: Add two big integers.
5. **Subtraction**: Subtract one big integer from another.
6. **Multiplication**: Multiply two big integers.
7. **Division**: Divide one big integer by another.
8. **Modulo**: Find the remainder of division between two big integers.
9. **Square Root**: Compute the floor integer value of the square root of a big integer.
10. **Exponentiation**: Raise a big integer to a power.
11. **Integer Conversion**: Convert a simple integer to a big integer.
12. **Fibonacci Calculation**: Compute Fibonacci numbers up to the 100,000th position.
13. **Factorial Calculation**: Compute factorials up to 1,000!.
14. **Catalan Numbers**: Calculate Catalan numbers up to the 1,000th position.
15. **Comparison**: Compare two big integers to determine which is greater or smaller.

## Implementation Details

### Storage

Big integers are stored in C++ strings in reverse order. This allows for efficient addition, subtraction, and multiplication operations by aligning digits from least significant to most significant.

### Operations

#### Addition/Subtraction

Addition and subtraction are performed digit-by-digit, similar to manual arithmetic. Carry-over values are managed and propagated as needed.

#### Multiplication

For multiplication, each digit of one number is multiplied by every digit of the other number. The results are then summed up with appropriate positional shifts.

#### Division and Modulo

Division and modulo operations are implemented using repeated subtraction or other efficient algorithms suited for large numbers.

#### Square Root

The square root operation finds the floor value of the square root using methods like binary search or Newton's method.

#### Exponentiation

Exponentiation is handled using repeated multiplication or more efficient algorithms like exponentiation by squaring.

### Advanced Calculations

- **Fibonacci**: Calculated using efficient iterative or matrix exponentiation techniques.
- **Factorial**: Computed using iterative multiplication.
- **Catalan Numbers**: Calculated using dynamic programming or direct formula implementation.

## Example Usage

### Creating and Initializing Big Integers

```cpp
BigInt num1("12345678901234567890");
BigInt num2(9876543210);
```

### Arithmetic Operations

```cpp
BigInt sum = num1 + num2;
BigInt diff = num1 - num2;
BigInt prod = num1 * num2;
BigInt quotient = num1 / num2;
BigInt remainder = num1 % num2;
BigInt power = num1.pow(5);
BigInt sqrtValue = num1.sqrt();
```

### Advanced Calculations

```cpp
BigInt fibonacci10000 = BigInt::fibonacci(10000);
BigInt factorial1000 = BigInt::factorial(1000);
BigInt catalan1000 = BigInt::catalan(1000);
```

### Comparison

```cpp
if (num1 > num2) {
    // num1 is greater than num2
} else {
    // num1 is less than or equal to num2
}
```

## Conclusion

The BigInt library is a comprehensive tool for handling large integers in C++, supporting a wide range of arithmetic and advanced mathematical operations. It is optimized for performance and accuracy, making it suitable for various applications requiring manipulation of very large numbers.