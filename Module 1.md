# Module 1

## 1. Write a python program to print the following integer literals 123,456,789

##  AIM
To write a Python program that prints the following integer literals separated by commas:  
**123, 456, 789**

---

##  Algorithm

1. **Start** the program.
2. Define the integer literals: `123`, `456`, and `789`.
3. Use the `print()` function to output the integers with commas in between.
4. **End** the program.

---

##  Python Code
```
# Program to print integer literals: 123, 456, 789

print(123, 456, 789)
```
## Output
![image](https://github.com/user-attachments/assets/1215bbc5-7448-486f-9bc8-bfdb37cfa0d9)

## 2. Write a python program to read and  then print the string.  men_stepped_on_the_moon= print()

##  AIM
To write a Python program that reads a string assigned to a variable and prints it.

---

##  Algorithm

1. **Start** the program.
2. Declare and assign a string to the variable `men_stepped_on_the_moon`.
3. Use the `print()` function to display the contents of the variable.
4. **End** the program.

---

##  Python Code

```
# Program to read and print the string

men_stepped_on_the_moon = "That's one small step for man, one giant leap for mankind."

print(men_stepped_on_the_moon)
```
## Output
![image](https://github.com/user-attachments/assets/159d6fbb-637e-44c7-bf47-d57004c2a5b4)

## 3. Write a python program to evaluate the following expression a+b*c-a/b

##  AIM
To write a Python program that evaluates the mathematical expression:  
**a + b * c - a / b**

---

##  Algorithm

1. **Start** the program.
2. Initialize variables `a`, `b`, and `c` with appropriate numeric values.
3. Use Python arithmetic operators to evaluate the expression:  
   `a + b * c - a / b`
4. Store the result in a variable (optional).
5. Use the `print()` function to display the result.
6. **End** the program.

---

## Python Code

```
# Program to evaluate the expression: a + b * c - a / b

a = 10
b = 5
c = 2

result = a + b * c - a / b

print("Result of the expression a + b * c - a / b is:", result)
```
## Output
![image](https://github.com/user-attachments/assets/6196219b-206c-45ef-8e39-ee71025cd895)

## 4. Write a Python program to read the value of m as an integer value from the user , According to the value of m, set and print the value of n using if..elif statements. The value of n is 1 when m is larger than 10, n is 0 when m is 10 and n is -1 when m is less than 10.
##  AIM
To write a Python program that reads an integer value `m` from the user,  
then sets and prints the value of `n` using `if..elif` statements based on the following conditions:

- `n = 1` when `m > 10`  
- `n = 0` when `m == 10`  
- `n = -1` when `m < 10`

---

##  Algorithm

1. **Start** the program.
2. Prompt the user to enter an integer and store it in variable `m`.
3. Use `if`, `elif`, and `else` statements to check the value of `m`:
   - If `m > 10`, set `n = 1`
   - Else if `m == 10`, set `n = 0`
   - Else, set `n = -1`
4. Print the value of `n`.
5. **End** the program.

---

##  Python Code

```
# Program to read m and set n based on its value

m = int(input("Enter an integer value for m: "))

if m > 10:
    n = 1
elif m == 10:
    n = 0
else:
    n = -1

print("The value of n is:", n)
```
## Output
![image](https://github.com/user-attachments/assets/4bb216b1-f39b-4169-bbc3-02f534b517be)

