# Module 5

## 1. Write a python program using class to perform addition of two numbers using parameterised constructor.

---

### AIM
To write a Python program that defines a class to perform the addition of two numbers using a parameterized constructor to initialize the numbers.

---

### Algorithm

1.  **Start** the program.
2.  Define a class, for example, `Addition`.
3.  Inside the class, define a parameterized constructor `__init__(self, num1, num2)` that takes two numbers as arguments.
4.  Store these arguments as instance variables (e.g., `self.num1`, `self.num2`).
5.  Define a method (e.g., `perform_addition`) within the class that calculates the sum of `self.num1` and `self.num2`.
6.  Print the original numbers and their sum within this method.
7.  Outside the class, prompt the user to input two numbers.
8.  Create an instance of the `Addition` class, passing the user-entered numbers to the constructor.
9.  Call the `perform_addition` method on the created object.
10. **End** the program.

---

### Python Code
```python
# Program to perform addition of two numbers using a parameterized constructor

class Addition:
    def __init__(self, num1, num2):
        """
        Constructor to initialize two numbers.
        """
        self.number1 = num1
        self.number2 = num2
        print("First number =", self.number1)
        print("Second number =", self.number2)

    def perform_addition(self):
        """
        Calculates and prints the sum of the two numbers.
        """
        sum_result = self.number1 + self.number2
        print("Addition of two numbers =", sum_result)

# Get input from the user
try:
    n1 = int(input())
    n2 = int(input())

    # Create an object of the Addition class, which calls the constructor
    adder = Addition(n1, n2)

    # Call the method to perform addition
    adder.perform_addition()

except ValueError:
    print("Invalid input. Please enter integers only.")
```
# Output
![image](https://github.com/user-attachments/assets/80160772-0d30-4206-ae00-f776dc3b1cf9)

---
---

## 2. Create a Python Class Student with a destructor.

---

### AIM
To create a Python class named `Student` that demonstrates the use of a destructor (`__del__`) to show when an object is being destroyed.

---

### Algorithm

1.  **Start** the program.
2.  Define a class named `Student`.
3.  Inside the `Student` class, define a constructor `__init__(self, name)` that initializes a student's name and prints a message indicating object initialization.
4.  Define a method (e.g., `display_name`) to print the student's name.
5.  Define a destructor `__del__(self)` that prints a message indicating object destruction.
6.  Outside the class, create an instance of the `Student` class.
7.  Call the `display_name` method.
8.  Explicitly delete the object using `del` (or allow it to go out of scope) to trigger the destructor.
9.  **End** the program.

---

### Python Code
```python
# Program to demonstrate a Python class with a destructor

class Student:
    def __init__(self, name):
        """
        Constructor to initialize the student object.
        """
        self.name = name
        print("Inside Constructor")
        print("Object initialized")

    def display_name(self):
        """
        Displays the student's name.
        """
        print(f"Hello, my name is {self.name}")

    def __del__(self):
        """
        Destructor to clean up resources (called when object is destroyed).
        """
        print("Inside destructor")
        print("Object destroyed")

# Create an object of the Student class
student1 = Student("Emma")

# Call a method on the object
student1.display_name()

# Explicitly delete the object to trigger the destructor
# Note: The destructor is called when the reference count to the object becomes zero.
# This might not happen immediately after `del` if other references exist.
del student1

# Any code here will execute after the object is (eventually) destroyed.
# You might not see "Object destroyed" immediately if the garbage collector
# hasn't run yet, but it will appear when the object is truly finalized.
```
# Output
![image](https://github.com/user-attachments/assets/3e58c384-6d98-4dcd-ab24-8aa69124ac0e)

---
---

## 3. Write a Python Program to Display the Employee Details
`EmpId , Emp Name.`

---

### AIM
To write a Python program that takes Employee ID and Employee Name as input and displays them as a tuple.

---

### Algorithm

1.  **Start** the program.
2.  Prompt the user to enter the Employee Name and store it in a variable (e.g., `emp_name`).
3.  Prompt the user to enter the Employee ID and store it in a variable (e.g., `emp_id`).
4.  Create a tuple containing the `emp_id` and `emp_name` in the desired order.
5.  Print the created tuple.
6.  **End** the program.

---

### Python Code
```python
# Program to display Employee Details

# Get Employee Name from user
emp_name = input()

# Get Employee ID from user
emp_id = int(input())

# Create a tuple with EmpId and EmpName
employee_details = (emp_id, emp_name)

# Display the employee details
print(employee_details)
```
# Output
![image](https://github.com/user-attachments/assets/66ed9f88-2889-4635-ad62-f5147de3fdce)

---
---

## 4. Write a Python program to Get the name, age and location of a person and display using Multilevel inheritance.

---

### AIM
To write a Python program that demonstrates multilevel inheritance by getting a person's name, age, and location and displaying them.

---

### Algorithm

1.  **Start** the program.
2.  Define a base class, e.g., `Person`, with a constructor to initialize the `name`.
3.  Define a derived class, e.g., `AgeInfo`, that inherits from `Person` and its constructor initializes `age` in addition to calling the base class constructor for `name`.
4.  Define another derived class, e.g., `LocationInfo`, that inherits from `AgeInfo` and its constructor initializes `location` in addition to calling the base class constructor for `name` and `age`.
5.  In the `LocationInfo` class, define a method (e.g., `display_details`) to print the `name`, `age`, and `location`.
6.  Outside the classes, prompt the user to input the name, age, and location.
7.  Create an instance of the `LocationInfo` class, passing the user-entered details to its constructor.
8.  Call the `display_details` method on the created object.
9.  **End** the program.

---

### Python Code
```python
# Program to demonstrate Multilevel Inheritance for person details

class Person:
    def __init__(self, name):
        self.name = name

class AgeInfo(Person):
    def __init__(self, name, age):
        super().__init__(name)  # Call base class constructor
        self.age = age

class LocationInfo(AgeInfo):
    def __init__(self, name, age, location):
        super().__init__(name, age) # Call immediate base class constructor
        self.location = location

    def display_details(self):
        print(f"{self.name} {self.age} {self.location}")

# Get input from the user
person_name = input()
person_age = int(input())
person_location = input()

# Create an object of the lowest-level derived class
person_details = LocationInfo(person_name, person_age, person_location)

# Display the details using the method from the derived class
person_details.display_details()
```
# Output
![image](https://github.com/user-attachments/assets/7ba87fee-209b-4bde-b6f1-f614a5695567)
