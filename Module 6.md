# Module 6

## 1. created two classes Ferrari and BMW. They have the same instance method names `fuel_type()` and `max_speed()`. However, we have not linked both the classes nor have we used inheritance. Pack two different objects into a `tuple` and iterate through it using a car variable.

---

### AIM
To demonstrate polymorphism by creating two unrelated classes, `Ferrari` and `BMW`, each with identical instance method names (`fuel_type()` and `max_speed()`), and then iterating through a tuple containing objects of both classes to call these methods.

---

### Algorithm

1.  **Start** the program.
2.  Define a class `Ferrari` with `fuel_type()` and `max_speed()` methods.
3.  Define a class `BMW` with `fuel_type()` and `max_speed()` methods.
4.  Create an instance of `Ferrari`.
5.  Create an instance of `BMW`.
6.  Pack both instances into a tuple.
7.  Iterate through the tuple using a loop variable, e.g., `car`.
8.  Inside the loop, call `car.fuel_type()` and `car.max_speed()`.
9.  **End** the program.

---

### Python Code
```python
class Ferrari:
    def fuel_type(self):
        print("Petrol")

    def max_speed(self):
        print("Max speed 350")

class BMW:
    def fuel_type(self):
        print("Diesel")

    def max_speed(self):
        print("Max speed is 240")

ferrari_obj = Ferrari()
bmw_obj = BMW()

cars = (ferrari_obj, bmw_obj)

for car in cars:
    car.fuel_type()
    car.max_speed()
```
# Output
![image](https://github.com/user-attachments/assets/484a77d8-ab41-4987-8a3e-fb50fbebefbc)

---
---

## 2. write a python program to perform addition of two complex number using binary '+' operator overloading
`class name : complex`

`Ob1 = complex(1, 2)`
`Ob2 = complex(2, 3)`

---

### AIM
To write a Python program that performs the addition of two complex numbers by overloading the binary `+` operator within a class named `Complex`.

---

### Algorithm

1.  **Start** the program.
2.  Define a class named `Complex`.
3.  Implement the constructor `__init__(self, real, imag)` to initialize the real and imaginary parts of the complex number.
4.  Overload the addition operator by defining the `__add__(self, other)` method.
5.  Inside `__add__`, calculate the new real part as `self.real + other.real`.
6.  Calculate the new imaginary part as `self.imag + other.imag`.
7.  Return a new `Complex` object with these new real and imaginary parts.
8.  Implement the `__repr__(self)` or `__str__(self)` method to provide a user-friendly string representation of the complex number.
9.  Create two `Complex` objects, `Ob1` and `Ob2`.
10. Add `Ob1` and `Ob2` using the `+` operator.
11. Print the result.
12. **End** the program.

---

### Python Code
```python
class Complex:
    def __init__(self, real, imag):
        self.real = real
        self.imag = imag

    def __add__(self, other):
        return Complex(self.real + other.real, self.imag + other.imag)

    def __str__(self):
        return f"({self.real}, {self.imag})"

Ob1 = Complex(1, 2)
Ob2 = Complex(2, 3)

Ob3 = Ob1 + Ob2

print(Ob3)
```
# Output
![image](https://github.com/user-attachments/assets/09c5530b-a1f7-4cbb-9876-2e9e228b3e7e)

---
---

## 3. import the `abc` module to create the abstract base class. Create the Car class that inherit the ABC class and define an abstract method named `mileage()`. then inherit the base class from the three different subclasses and implement the abstract method differently. Create the objects to call the abstract method.

---

### AIM
To demonstrate abstract base classes (ABCs) and polymorphism by creating an abstract `Car` class with an abstract `mileage()` method, then inheriting from it to create concrete subclasses that implement `mileage()` differently, and finally calling `mileage()` on objects of these subclasses.

---

### Algorithm

1.  **Start** the program.
2.  Import `ABC` and `abstractmethod` from the `abc` module.
3.  Define an abstract base class `Car` that inherits from `ABC`.
4.  Inside `Car`, define an abstract method `mileage()` using the `@abstractmethod` decorator. This method will have no implementation in the base class.
5.  Define three concrete subclasses (e.g., `Maruti`, `Honda`, `Hyundai`), each inheriting from `Car`.
6.  In each subclass, implement the `mileage()` method to return or print a specific mileage value.
7.  Create objects for each of the three subclasses.
8.  Call the `mileage()` method on each object.
9.  **End** the program.

---

### Python Code
```python
from abc import ABC, abstractmethod

class Car(ABC):
    @abstractmethod
    def mileage(self):
        pass

class Maruti(Car):
    def mileage(self):
        print("The mileage is 30kmph")

class Honda(Car):
    def mileage(self):
        print("The mileage is 27kmph")

class Hyundai(Car):
    def mileage(self):
        print("The mileage is 25kmph")

class Tata(Car):
    def mileage(self):
        print("The mileage is 24kmph")

maruti_obj = Maruti()
maruti_obj.mileage()

honda_obj = Honda()
honda_obj.mileage()

hyundai_obj = Hyundai()
hyundai_obj.mileage()

tata_obj = Tata()
tata_obj.mileage()
```
# Output 
![image](https://github.com/user-attachments/assets/ec869005-1519-45a9-ba30-a8c8d548c1dc)

---
---

## 4. Create a class Employee with public method show to display the details of the employee.

---

### AIM
To create a Python class named `Employee` with a public method `show()` that displays the name and salary of an employee.

---

### Algorithm

1.  **Start** the program.
2.  Define a class named `Employee`.
3.  Implement a constructor `__init__(self, name, salary)` to initialize the `name` and `salary` attributes.
4.  Define a public method `show(self)` within the class.
5.  Inside the `show()` method, print the employee's `name` and `salary`.
6.  Create an instance of the `Employee` class, providing a name and salary.
7.  Call the `show()` method on the created object.
8.  **End** the program.

---

### Python Code
```python
class Employee:
    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

    def show(self):
        print(f"Name: {self.name} Salary: {self.salary}")

emp1 = Employee("Jessa", 10000)
emp1.show()
```
# Output
![image](https://github.com/user-attachments/assets/1355f6ad-9842-4c9e-ab52-f34e1dbc92ec)
