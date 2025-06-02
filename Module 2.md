# Module 2  
 

---

## 1. Write a Python program to print even numbers from 1 to n

### AIM  
To write a Python program that prints all even numbers from 1 to a user-given number `n`.

---

### Algorithm

1. **Start** the program.  
2. Prompt the user to enter a value for `n`.  
3. Use a `for` loop to iterate from 1 to `n`.  
4. Check if a number is even using the condition `number % 2 == 0`.  
5. Print the even numbers.  
6. **End** the program.  

---

### Python Code
```
# Program to print even numbers from 1 to n

n = int(input("Enter the value of n: "))

print("Even numbers from 1 to", n, "are:")
for i in range(1, n + 1):
    if i % 2 == 0:
        print(i, end=' ')
```
## output
![image](https://github.com/user-attachments/assets/372cca92-dee7-4c1c-9099-8021be99c6af)

## 2. Write a Python program to define a function that accepts 2 values and returns their modulo value

## AIM

To write a Python function that accepts two numbers and returns the modulo (remainder after division) of the first by the second.

## Algorithm
Start the program.

Define a function find_modulo(a, b).

Inside the function, return a % b.

Get two inputs from the user.

Call the function and print the result.

End the program.


```
# Program to find the modulo of two numbers using a function

def find_modulo(a, b):
    return a % b

x = int(input("Enter the first number: "))
y = int(input("Enter the second number: "))

print("Modulo of", x, "and", y, "is:", find_modulo(x, y))
```
## Output
![image](https://github.com/user-attachments/assets/fc3813fe-dd1f-4065-b63e-bd41601bcc9e)

3. Write a lambda function which takes z as a parameter and returns z * 11

## AIM
To write a Python lambda function that takes an input z and returns z * 11.

## Algorithm
Start the program.

Define a lambda function: multiply_by_11 = lambda z: z * 11.

Get input for z from the user.

Call the lambda function and print the result.

End the program.
```
# Lambda function to multiply a number by 11

multiply_by_11 = lambda z: z * 11

z = int(input("Enter a number: "))
print("Result of z * 11 is:", multiply_by_11(z))
```
## Output
![image](https://github.com/user-attachments/assets/cbeefbac-5398-487d-befe-976805e652f9)

## 4. Write a Python program to print an inverted pyramid pattern with the same digit

##  AIM *

To write a Python program that prints an inverted pyramid pattern with the same digit, based on user input.

## Algorithm
Start the program.

Prompt the user to enter the number of rows.

Use nested loops to print the inverted pyramid:

Outer loop for rows (from input down to 1).

Inner loop to print the digit multiple times based on the current row.

Use print() with formatting to align the pyramid.

End the program.

```
# Inverted pyramid pattern with same digit

rows = int(input("Enter number of rows: "))
digit = int(input("Enter a digit to print in the pattern: "))

for i in range(rows, 0, -1):
    print(" " * (rows - i) + str(digit) * (2 * i - 1))
```
## Output

![image](https://github.com/user-attachments/assets/c7512582-66af-447f-b622-8bcf32fc2a5d)
