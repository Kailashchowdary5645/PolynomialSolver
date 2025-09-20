PolynomialSolver – Java Implementation for Constant Term Calculation

This repository contains a Java program to compute the constant term (c) of a polynomial given a set of roots in various bases. It works with JSON input files specifying roots and their numeric bases, making it flexible for large numbers and multiple test cases.

Features

Input Format: Accepts a JSON file with:

keys.n – total number of roots provided.

keys.k – minimum number of roots required to compute the polynomial coefficients (degree m = k-1).

Root objects with:

"base": numeric base of the root value.

"value": root value as a string.

Base Conversion: Supports bases up to 36, allowing roots in decimal, binary, octal, hexadecimal, or any custom base within 2–36.

Lagrange Interpolation: Uses Lagrange interpolation to calculate the constant term (c) of the polynomial at x = 0.

BigInteger Support: Handles extremely large roots safely without integer overflow using Java’s BigInteger.

Outputs: Prints only the constant term to standard output, making it suitable for automated testing or further calculations.

How to Use

Compile the Program

javac ConstantTerm.java

Run with a JSON Input File

java ConstantTerm < test_case_1.json

Example Output

3
Test Cases

Test Case 1 (test_case_1.json):

n = 4, k = 3

Roots in bases: 10, 2, 10, 4

Output: 3

Test Case 2 (test_case_2.json):

n = 10, k = 7

Roots in bases: 6, 15, 15, 16, 8, 3, 3, 6, 12, 7

Output: 7

Repository Structure
PolynomialSolver/
├── ConstantTerm.java       # Java implementation for computing the constant term
├── test_case_1.json        # Sample test case 1
├── test_case_2.json        # Sample test case 2
└── README.md               # Project description and usage instructions
Advantages

Supports very large integers using BigInteger.

Handles roots in multiple bases.

Easy to extend for additional polynomial computations.

Self-contained and requires no external libraries.
