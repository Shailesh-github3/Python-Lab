# Module 4
## HARI NIVEDHAN

## 1. Print the value of the key 'history' from the given dictionary.
`sampleDict = { "class": { "student": { "name": "Mike", "marks": { "physics": 70, "history": 80 } } } }`

### AIM
To write a Python program that accesses and prints the value associated with the key 'history' from a nested dictionary.

---

### Algorithm

1. **Start** the program.
2. Define the given nested dictionary `sampleDict`.
3. Access the 'history' value by navigating through the nested keys: `'class'`, `'student'`, `'marks'`, and then `'history'`.
4. Use the `print()` function to display the extracted value.
5. **End** the program.

---

### Python Code
```python
# Program to print the value of the 'history' key from a nested dictionary

sampleDict = {
    "class": {
        "student": {
            "name": "Mike",
            "marks": {
                "physics": 70,
                "history": 80
            }
        }
    }
}

# Accessing the value of 'history'
history_marks = sampleDict["class"]["student"]["marks"]["history"]

# Printing the value
print("History marks:", history_marks)
```
# Output

![image](https://github.com/user-attachments/assets/da601f17-88ad-413b-9d45-19c4bb06676a)

---

## 2. Write a python code to check if the value given in age as input is negative and then force the program to raise an exception using `raise` keyword.

### AIM
To write a Python program that takes an age as input, checks if it's negative, and if so, raises a custom `ValueError` exception.

---

### Algorithm

1. **Start** the program.
2. Prompt the user to enter their age using `input()` and convert it to an integer.
3. Use an `if` statement to check if the entered `age` is less than 0.
4. If `age` is negative, use the `raise` keyword to explicitly raise a `ValueError` with an informative message.
5. If `age` is not negative, print a confirmation message.
6. Use a `try-except` block to gracefully handle the raised `ValueError` and print the exception message.
7. **End** the program.

---

### Python Code
```python
# Program to check for negative age input and raise an exception

try:
    age = int(input("Enter your age: "))

    if age < 0:
        raise ValueError("Age cannot be negative!")
    else:
        print("Your age is:", age)

except ValueError as e:
    print("Error:", e)
```

# Output

![image](https://github.com/user-attachments/assets/6939f999-654e-402e-b4aa-f8efc009b2b6)

---

## 3. Write a Python program to read a file and count the frequency of each character in it.

### AIM
To write a Python program that reads the content of a text file and then calculates and displays the frequency of each character present in the file.

---

### Algorithm

1. **Start** the program.
2. Define the filename to be read.
3. Initialize an empty dictionary (e.g., `char_frequency`) to store character counts.
4. Open the file in read mode (`'r'`).
5. Read the entire content of the file.
6. Iterate through each character in the file content:
   - For each character, check if it's already a key in `char_frequency`.
   - If it is, increment its corresponding value by 1.
   - If it's not, add the character as a new key with a value of 1.
7. Close the file.
8. Print the character frequencies.
9. **End** the program.

---

### Python Code
```python
# Program to count the frequency of each character in a file

def count_char_frequency(filename):
    char_frequency = {}
    try:
        with open(filename, 'r') as file:
            content = file.read()
            for char in content:
                char_frequency[char] = char_frequency.get(char, 0) + 1
    except FileNotFoundError:
        print(f"Error: The file '{filename}' was not found.")
        return None
    return char_frequency

# Create a dummy file for demonstration
with open("sample.txt", "w") as f:
    f.write("Hello World!\n")
    f.write("Python programming.")

filename = "sample.txt"
frequencies = count_char_frequency(filename)

if frequencies:
    print(f"Character frequencies in '{filename}':")
    for char, count in sorted(frequencies.items()):
        print(f"'{char}': {count}")
```

---
# Output

![image](https://github.com/user-attachments/assets/fd299629-081a-4879-9ec8-cf4bb4f0cccf)

## 4. Write Python Program to take the radius from the user and find the area of the circle using class name 'cse' and function name 'mech'

### AIM
To write a Python program that defines a class named `cse` with a method named `mech` to calculate the area of a circle, taking the radius as input from the user.

---

### Algorithm

1. **Start** the program.
2. Define a class named `cse`.
3. Inside the `cse` class, define a method named `mech` that takes `self` and `radius` as arguments.
4. Inside the `mech` method, calculate the area of the circle using the formula: `Area = π * radius^2` (use `math.pi` for π).
5. Print the calculated area.
6. Outside the class, prompt the user to enter the radius of the circle and convert it to a float.
7. Create an instance (object) of the `cse` class.
8. Call the `mech` method on the object, passing the user-provided radius.
9. **End** the program.

---

### Python Code
```python
# Program to calculate the area of a circle using a class and method

import math

class cse:
    def mech(self, radius):
        """
        Calculates and prints the area of a circle.
        """
        if radius < 0:
            print("Radius cannot be negative.")
            return

        area = math.pi * (radius ** 2)
        print(f"The area of the circle with radius {radius} is: {area:.2f}")

# Get radius from the user
try:
    user_radius = float(input("Enter the radius of the circle: "))

    # Create an instance of the cse class
    my_circle = cse()

    # Call the mech method to calculate and print the area
    my_circle.mech(user_radius)

except ValueError:
    print("Invalid input. Please enter a numeric value for the radius.")
```
# Output

![image](https://github.com/user-attachments/assets/94ce35c3-9fce-4ec8-8c2f-606b5a41c0bc)
