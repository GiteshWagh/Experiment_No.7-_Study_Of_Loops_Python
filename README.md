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


```python
# Problem :
# Write a Python program for matrix multiplication (if possible)

# Solution :
# Taking input from the user for both matrix A & B
row1 = int(input("Enter rows for Matrix A: "))
col1 = int(input("Enter columns for Matrix A: "))
row2 = int(input("Enter rows for Matrix B: "))
col2 = int(input("Enter columns for Matrix B: "))

# Checking if the matrix multiplication is possible
# For multiplication the number of columns of matrix A should be equal to number columns of matrix B.
if col1 != row2:
    print(f"Cannot multiply! Columns of A ({col1}) must equal Rows of B ({row2}).")
else:

    print(f"\nFill Matrix A ({row1}x{col1}):")
    matrix_A = [] # Matrix A
    for i in range(row1):
        row = []
        for j in range(col1):
            val = int(input(f"Enter element A[{i+1}][{j+1}]: "))
            row.append(val)
        matrix_A.append(row)


    print(f"\nFill Matrix B ({row2}x{col2}):")
    matrix_B = [] # Matrix B
    for i in range(row2):
        row = []
        for j in range(col2):
            val = int(input(f"Enter element B[{i+1}][{j+1}]: "))
            row.append(val)
        matrix_B.append(row)

    result = []
    for i in range(row1):
        row = []
        for j in range(col2):
            row.append(0)
        result.append(row)


    for i in range(row1):
        for j in range(col2):
            for k in range(col1):
                result[i][j] += matrix_A[i][k] * matrix_B[k][j]

# Printing the resultant matrix with the help of for loop for proper structure.
    print("\n--- The Resulting Matrix ---")
    for row in result:
        # We use a loop here too to print nicely
        for element in row:
            print(element, end=" ")
        print() # For new line after each row
```

### Algorithm & Explanation:
1. Start by taking the number of rows and columns for two matrices, $A$ and $B$.
2. **Check Condition:** If columns of $A$ do not equal rows of $B$, multiplication is impossible.
3. If valid, take user input to fill both matrices using nested loops.
4. Create a result matrix filled with zeros.
5. Use a triple-nested loop ($i, j, k$) to multiply elements and add them to the result matrix.
6. Print the final result in a structured grid format.  

---

```python
# Problem :
# Write a Python code for Floyd's series

# Solution :
n = int(input("How many layers you want : "))
a=1
for i in range(n+1):
  for j in range(i):
    print(a,end=" ")
    a = a +1
  print(" ")
```
### Algorithm & Explanation:
* Step 1: Start the program and take the number of layers (n) as input from the user.
* Step 2: Initialize a variable a with the value 1 to act as the starting number of the series.
* Step 3: Start an outer for loop that runs from 0 to n to manage the total number of rows.
* Step 4: Inside the outer loop, start a nested for loop that runs i times to control the number of elements in the current row.
* Step 5: Print the current value of a followed by a space, using end=" " to keep the output on the same line.
* Step 6: Increment the value of a by 1 (a = a + 1) after each print to prepare the next number in the sequence.
* Step 7: Execute a print(" ") statement after the inner loop finishes to move the cursor to a new line for the next row.
* Step 8: Terminate the program once all iterations of the loops are complete.
  
---
```python
# Problem Statement :
# Write a code to print all the prime numbers in given range.

# Solution :
n = int(input("Enter the starting number : "))
m = int(input("Enter the ending number : "))
for num in range(n,m+1):
  for i in range(2,num):
    if num%i==0:
      break
  else:
    print(num,end=" ")
```
### Algorithm & Explanation:
* Step 1: The outer loop picks a number (num) from the user's range.
* Step 2: The inner loop tries dividing that number by every integer from 2 up to num - 1.
* Step 3: If the remainder is 0 (num % i == 0), it means the number has a factor other than 1 and itself, so it’s not prime. We use break to stop checking.
* Step 4: If the inner loop finishes without hitting a break, the else block executes and prints the prime number.
---
```python
```
---

```python
# Problem :
# Write a code to print Diamond shape

# Solution :
n = 5
for i in range(n,0,-1):
  print(i*" ",(n-i)*"* ")
for i in range(n):
  print(i*" ",(n-i)*"* ")
```
### Algorithm & Explanation:
* Step 1: Initialize the variable n with a value (e.g., 5) to determine the overall size and height of the diamond.
* Step 2: Start the first for loop to handle the top half of the diamond, iterating from n down to 0.
* Step 3: Inside the first loop, print a specific number of spaces calculated by multiplying the space character " " by the current loop index i.
* Step 4: On the same line, print the stars by multiplying the string "* " by the difference (n - i).
* Step 5: Start the second for loop to handle the bottom half of the diamond, iterating from 0 up to n.
* Step 6: Inside the second loop, print leading spaces by multiplying " " by the current loop index i.
* Step 7: On the same line, print the stars by multiplying the string "* " by the difference (n - i).
* Step 8: End the program once both loops have finished printing all rows.

---
```python
# Problem:
# Write a code to print 2D plane with stars symbol(*)

# Solution :
n = 5
for i in range(n):
  print(i*" ",(n)*" * ")
```
### Algorithm & Explanation:
* Step 1: Initialize the variable n with a value (e.g., 5) to define the number of rows and the width of the pattern.
* Step 2: Start a for loop that iterates n times to manage the total number of rows.
* Step 3: Inside the loop, print leading spaces by multiplying the space character " " by the current loop index i to create a slanted effect.
* Step 4: On the same line, print a fixed number of stars by multiplying the string " * " by the value of n.
* Step 5: Repeat these steps for each iteration, which shifts each subsequent row to the right.
* Step 6: Terminate the program once the loop has completed all n iterations.
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
