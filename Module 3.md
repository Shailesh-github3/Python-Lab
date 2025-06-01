# Module 3  
## HARI NIVEDHAN  

---

## 1. Write a Python function that accepts a string and converts it into uppercase, lowercase, and title case.

### AIM  
To write a Python function that accepts a string and displays it in uppercase, lowercase, and title case formats.

---

### Algorithm

1. **Start** the program.  
2. Define a function `convert_cases(text)` that:
   - Converts the string to uppercase using `.upper()`.
   - Converts the string to lowercase using `.lower()`.
   - Converts the string to title case using `.title()`.
3. Get the string input from the user.  
4. Call the function with the input string.  
5. **End** the program.  

---

### Python Code
```
# Function to convert string to upper, lower, and title case

def convert_cases(text):
    print("Uppercase:", text.upper())
    print("Lowercase:", text.lower())
    print("Title Case:", text.title())

user_input = input("Enter a string: ")
convert_cases(user_input)
```
# Output
![image](https://github.com/user-attachments/assets/5d3ab23d-1f35-45b9-85ff-bbe43314417b)

## 2. Create a Python program to replace all occurrences of 5 with "five" for the given string
# AIM
To write a Python program that replaces all occurrences of the digit 5 with the word "five" in a given string.

# Algorithm
Start the program.

Get a string input from the user.

Use the replace() method to replace '5' with 'five'.

Print the updated string.

End the program.

# Program to replace all occurrences of 5 with 'five'
```
text = input("Enter a string: ")
updated_text = text.replace('5', 'five')
print("Updated string:", updated_text)
```
# Output
![image](https://github.com/user-attachments/assets/4f6bbdf6-0a7c-42a8-93e0-b041fa4d888b)

## 3. Write a non-parameterized function to print the list in descending order that is entered by the user
# AIM
To write a non-parameterized Python function that reads a list from the user and prints it in descending order.

# Algorithm
Start the program.

Define a function print_descending() without parameters.

Inside the function:

Accept input from the user, split it into list elements, and convert to integers.

Sort the list in descending order using sort(reverse=True).

Print the sorted list.

Call the function.

End the program.

```
# Non-parameterized function to print list in descending order

def print_descending():
    numbers = list(map(int, input("Enter numbers separated by space: ").split()))
    numbers.sort(reverse=True)
    print("List in descending order:", numbers)

print_descending()
```
# Output
![image](https://github.com/user-attachments/assets/0ff08325-1eff-4d64-9589-da34009ae343)


## 4. Write a Python program to create a tuple using the numbers entered by the user.Get the size of the tuple from the user.
# AIM
To write a Python program that creates a tuple with user-entered numbers and prints it.

# Algorithm
Start the program.

Ask the user to enter the size of the tuple.

Use a loop to get individual numbers from the user.

Store the numbers in a list.

Convert the list to a tuple.

Print the final tuple.

End the program.

```
# Program to create a tuple using user-entered numbers

size = int(input("Enter the size of the tuple: "))
elements = []

for i in range(size):
    num = int(input(f"Enter element {i+1}: "))
    elements.append(num)

result_tuple = tuple(elements)
print("The created tuple is:", result_tuple)
```
# output 
![image](https://github.com/user-attachments/assets/e876f70f-2ecf-4f06-bc37-c5fa54620c5b)
