# Experiment: Study of Iterative Structures (Loops) in Python

## Aim : 
The primary aim of this practical is to study and implement different types of loops in Python. The experiment focuses on understanding how to automate repetitive tasks and solve complex logic problems using iterative structures.

## Objects :
Our main objectives were:
* To master the **While Loop** for condition-based iteration.
* To master the **For Loop** for range-based and sequence-based iteration.
* To understand **Nested Loops** for solving multi-dimensional problems like matrix multiplication and combinations.
* To learn loop control statements like `break` and `continue` to modify the flow of an iteration.

---

## Theory and Concepts Used

### 1. The While Loop
A `while` loop is used when we want to repeat a block of code as long as a specific condition is true. In this practical, I used it for simple counting and for reversing strings to check for palindromes. It is essential when the number of iterations isn't known beforehand.

### 2. The For Loop
The `for` loop is used to iterate over a sequence (like a list or a string) or a range of numbers. It is the most common loop used in Python for fixed-length iterations, such as generating Armstrong numbers within a specific range.

### 3. Loop Control: The `continue` Statement
Sometimes we need to skip a specific part of a loop without stopping the whole thing. The `continue` statement allows the program to jump back to the start of the loop for the next iteration, skipping any code written below it for that specific turn.

### 4. Nested Loops
When a loop is placed inside another loop, it is called a nested loop. This is a powerful concept used in this experiment for:
* **Matrix Multiplication:** Iterating through rows and columns.
* **Combinations:** Generating all possible sets of three digits.
* **Pattern Printing:** Managing spaces and stars to create a diamond shape.
---

# Problem :
# Write a Python code for Floyd's series

# Solution :
```python
n = int(input("How many layers you want : "))
a=1
for i in range(n+1):
  for j in range(i):
    print(a,end=" ")
    a = a +1
  print(" ")
```

### Algorithm & Explanation:
*** Step 1:** We first check the "Gold Rule" of matrices: the number of columns in Matrix A must match the rows in Matrix B.
**Step 2:** We create a "Result" matrix filled with zeros to store our answers.
**Step 3:** We use three nested loops. The first two loops ($i$ and $j$) navigate through the rows and columns of the result matrix.
//Step 4:** The third loop ($k$) performs the "dot product". it multiplies the elements of A's row by B's column and adds them to our result.

---

## Practical Applications Implemented

| Experiment Task | Loop Type Used | Logic Applied |
| :--- | :--- | :--- |
| **Basic Counter** | `while` | Incrementing a variable until it reaches $N$. |
| **Palindrome Checker** | `while` | Using a loop to read a string backward and store it in a new variable. |
| **Iterative Skip** | `while` + `continue` | Skipping the print command specifically when the counter hits 5. |
| **Matrix Multiplication**| Triple `for` loops | Using $i, j, k$ loops to calculate the dot product of rows and columns. |
| **Digit Combinations** | Triple `for` loops | Three nested loops to find all unique permutations of 3 numbers. |
| **Armstrong Finder** | `for` | Iterating through a mathematical range and calculating the sum of powers. |
| **Diamond Pattern** | `for` | Using two separate loops (one for the top, one for the bottom) to print shapes. |

---

## Conclusion
Through this experiment, I have gained a deep understanding of how loops work in Python. I successfully implemented simple counters, conditional skips, and complex nested structures for matrix math. Understanding loops is fundamental to programming because it allows us to handle large amounts of data and perform repetitive calculations efficiently.

---
*Submitted by: Gitesh Wagh*
*Course: B.Tech (E&TC)*
