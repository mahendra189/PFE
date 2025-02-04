# Python For Engineers

### **1. Program to Calculate the Area of a Circle and Triangle**
```python
# 1.py
PI = 3.14

def area_circle(radius):
    return PI * radius ** 2

def area_triangle(base, height):
    return 0.5 * base * height

# Example usage
print("Area of circle:", area_circle(5))
print("Area of triangle:", area_triangle(4, 3))
```

---

### **2. Program to Swap Two Variables**
```python
# 2.py
a = 5
b = 10
a, b = b, a
print("After swapping:", a, b)
```

---

### **3. Program to Generate a Random Number**
```python
# 3.py
import random
print("Random number:", random.randint(1, 100))
```

---

### **4. Program to Convert Kilometers to Miles**
```python
# 4.py
def km_to_miles(km):
    return km * 0.621371

# Example usage
print("5 km in miles:", km_to_miles(5))
```

---

### **5. Program to Find Maximum of Two Numbers**
```python
# 5.py
def max_of_two(a, b):
    return a if a > b else b

# Example usage
print("Max of 10 and 20:", max_of_two(10, 20))
```

---

### **6. Program to Check if a Number is Even or Odd**
```python
# 6.py
def check_even_odd(num):
    return "Even" if num % 2 == 0 else "Odd"

# Example usage
print("10 is:", check_even_odd(10))
```

---

### **7. Program to Check if a Number is Positive, Negative or Zero**
```python
# 7.py
num = 6

print("6 is ")
if num > 0:
    print("Positive")
elif num < 0:
    print("Negative")
else:
    print("Zero")
```

---

### **8. Program to Calculate Minimum Number of Desks Needed for Three Classes**
```python
# 8.py
def calculate_desks(class1, class2, class3):
    return (class1 + class2 + class3 + 1) // 2

# Example usage
print("Desks needed:", calculate_desks(20, 21, 22))
```

---

### **9. Program to Calculate the Angle of the Hour Hand on a Clock**
```python
# 9.py
def hour_angle(hours, minutes, seconds):
    total_seconds = hours * 3600 + minutes * 60 + seconds
    angle = (total_seconds / 43200) * 360
    return angle % 360

# Example usage
print("Hour hand angle:", hour_angle(3, 15, 0))
```

---

### **10. Program to Find the Fourth Vertex of a Rectangle**
```python
# 10.py
def fourth_vertex(v1, v2, v3):
    x = v1[0] + v2[0] + v3[0] - 2 * min(v1[0], v2[0], v3[0])
    y = v1[1] + v2[1] + v3[1] - 2 * min(v1[1], v2[1], v3[1])
    return (x, y)

# Example usage
print("Fourth vertex:", fourth_vertex((0, 0), (2, 0), (0, 3)))
```

---

### **11. Program to Find the Missing Card Number**
```python
# 11.py
def missing_card(cards):
    n = len(cards) + 1
    total = n * (n + 1) // 2
    return total - sum(cards)

# Example usage
print("Missing card:", missing_card([1, 2, 4, 5]))
```

---

### **12. Program to Find Maximum of Three Numbers**
```python
# 12.py
def max_of_three(a, b, c):
    if a>b:
        if a>c:
            return a
        else:
            return c
    elif b>c:
        return b
    else:
        return c
# Example usage
print("Max of 10, 20, 30:", max_of_three(10, 20, 30))
```

---

### **13. Program to Check if a Year is Leap**
```python
# 13.py
def is_leap(year):
    return year % 4 == 0 and (year % 100 != 0 or year % 400 == 0)

# Example usage
print("Is 2024 a leap year?", is_leap(2024))
```

---

### **14. Program to Check if a Date is Valid**
```python
# 14.py
def is_valid_date(year, month, day):
    def is_leap(year):
        return year % 4 == 0 and (year % 100 !=0 or year % 400 == 0)
    if month < 1 or month > 12:
        return False
    if day < 1 or day > 31:
        return False
    if month in {4, 6, 9, 11} and day > 30:
        return False
    if month == 2:
        if is_leap(year):
            return day <= 29
        else:
            return day <= 28
    return True

# Example usage
print("Is 2023-02-29 valid?", is_valid_date(2023, 2, 29))
```

---

### **15. Program to Find the Roots of a Quadratic Equation**
```python
# 15.py
import math

def quadratic_roots(a, b, c):
    discriminant = b**2 - 4*a*c
    if discriminant < 0:
        return "No real roots"
    elif discriminant == 0:
        return -b / (2*a)
    else:
        root1 = (-b + math.sqrt(discriminant)) / (2*a)
        root2 = (-b - math.sqrt(discriminant)) / (2*a)
        return root1, root2

# Example usage
print("Roots of x^2 - 5x + 6:", quadratic_roots(1, -5, 6))
```

---

### **16. Program to Remove Characters at Indices Divisible by 3 from a String**
```python
# 16.py
def remove_chars(s):
    return ''.join([s[i] for i in range(len(s)) if i % 3 != 0])

# Example usage
print("Result:", remove_chars("abcdefgh"))
```

---

### **17. Program to Find the Length of the Longest Sequence of Equal Elements in an Integer List**
```python
# 17.py
def longest_sequence(lst):
    max_len = 1
    current_len = 1
    for i in range(1, len(lst)):
        if lst[i] == lst[i-1]:
            current_len += 1
            max_len = max(max_len, current_len)
        else:
            current_len = 1
    return max_len

# Example usage
print("Longest sequence length:", longest_sequence([1, 2, 2, 3, 3, 3, 4]))
```

---

### **18. Program to Determine Which Bowling Pins Remain Standing**
```python
# 18.py
def bowling_pins_standing(pins, rolls):
    for roll in rolls:
        if 1 <= roll <= 10:
            pins[roll-1] = 0
    return [i+1 for i, x in enumerate(pins) if x == 1]

# Example usage
print("Pins standing:", bowling_pins_standing([1]*10, [2, 4, 6]))
```

---

### **19. Program to Calculate the Number of Seconds Between Two Timestamps**
```python
# 19.py
def take_timestamp():
    """Takes timestamp input from user and returns (hour, minute, second)."""
    print("Enter the timestamp: ")
    hour = int(input("Hour: "))
    minute = int(input("Minutes: "))
    second = int(input("Seconds: "))
    return hour, minute, second


def validate_timestamps(t1, t2):
    """Checks if t2 is later than t1, otherwise exits."""
    if t1 >= t2:
        print("Error: The second timestamp should be later than the first one.")
        exit()
    

def print_time(timestamp):
    """Formats timestamp as HH:MM:SS string."""
    return f"{timestamp[0]:02}:{timestamp[1]:02}:{timestamp[2]:02}"


# Take timestamps from the user
t1 = take_timestamp()
t2 = take_timestamp()

# Validate timestamps
validate_timestamps(t1, t2)

# Calculate differences
hour_diff = t2[0] - t1[0]
min_diff = t2[1] - t1[1]
sec_diff = t2[2] - t1[2]

# Adjust if seconds or minutes go negative (borrow from higher units)
if sec_diff < 0:
    sec_diff += 60
    min_diff -= 1

if min_diff < 0:
    min_diff += 60
    hour_diff -= 1

# Calculate total difference in seconds
total_seconds = (hour_diff * 3600) + (min_diff * 60) + sec_diff

# Output results
print(f"\nTimestamp 1: {print_time(t1)}")
print(f"Timestamp 2: {print_time(t2)}")
print(f"Time Difference: {hour_diff} hours, {min_diff} minutes, {sec_diff} seconds")
print(f"Total Difference: {total_seconds} seconds")

```

---

### **20. Program to Display First N Natural Numbers**
```python
# 20.py
def display_natural_numbers(n):
    for i in range(1, n+1):
        print(i, end=" ")

# Example usage
display_natural_numbers(10)
```

---

### **21. Program to Calculate Factorial of a Number**
```python
# 21.py
def factorial(n):
    if n<=1:
        return 1
    return n * factorial(n)

# Example usage
print("Factorial of 5:", factorial(5))
```

---

### **22. Program to Display Numbers in Reverse Order**
```python
# 22.py
def display_reverse(n):
    for i in range(n, 0, -1):
        print(i, end=" ")

# Example usage
display_reverse(10)
```

---

### **23. Program to Check if a Number is Prime**
```python
# 23.py
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5)+1):
        if n % i == 0:
            return False
    return True

# Example usage
print("Is 17 prime?", is_prime(17))
```

---

### **24. Program to Calculate Sum and Average of First N Numbers**
```python
# 24.py
def sum_and_avg(n):
    total = n * (n + 1) // 2
    avg = total / n
    return total, avg

# Example usage
print("Sum and average of first 10 numbers:", sum_and_avg(10))
```

---

### **25. Program to Display First N Multiples of a Given Number**
```python
# 25.py
def display_multiples(num, n):
    for i in range(1, n+1):
        print(num * i, end=" ")

# Example usage
display_multiples(5, 10)
```

---

### **26. Program to Display First N Fibonacci Numbers**
```python
# 26.py
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        print(a, end=" ")
        a, b = b, a + b

# Example usage
fibonacci(10)
```

---

### **27. Program to Find the Sum of Digits of a Number**
```python
# 27.py
def sum_of_digits(num):
    return sum(int(digit) for digit in str(num))

# Example usage
print("Sum of digits of 1234:", sum_of_digits(1234))
```

---

### **28. Program to Create and View Elements of a List**
```python
# 28.py
my_list = [1, 2, 3, 4, 5]
print("List elements:", my_list)
```

---

### **29. Program to Create and View Elements of a Tuple**
```python
# 29.py
my_tuple = (1, 2, 3, 4, 5)
print("Tuple elements:", my_tuple)
```

---

### **30. Program to Access List Indices and Values**
```python
# 30.py
my_list = [10, 20, 30, 40, 50]
for index, value in enumerate(my_list):
    print(f"Index: {index}, Value: {value}")
```

---

### **31. Program to Add Two Lists**
```python
# 31.py
list1 = [1, 2, 3]
list2 = [4, 5, 6]
result = list1 + list2
print("Combined list:", result)
```

---

### **32. Program to Check if a List is Empty or Not**
```python
# 32.py
def is_empty(lst):
    return len(lst) == 0

# Example usage
print("Is list empty?", is_empty([]))
```

---

### **33. Program to Find the Largest Number in a List**
```python
# 33.py
def find_largest(lst):
    return max(lst)

# Example usage
print("Largest number:", find_largest([10, 20, 30, 40]))
```

---

### **34. Program to Find the Second Largest Number in a List**
```python
# 34.py
def second_largest(lst):
    if len(lst) ==0:
        return -1
    if len(lst) < 2:
        return lst[0]
    return sorted(lst)[-2]

# Example usage
print("Second largest number:", second_largest([10, 20, 30, 40]))
```

---

### **35. Program to Separate Even and Odd Elements into Two Different Lists**
```python
# 35.py
def separate_even_odd(lst):
    even = []
    odd = []
    for x in lst:
        if x % 2 ==0:
            even.append(x)
        else:
            odd.append(x)
    return even, odd

# Example usage
print("Even and odd lists:", separate_even_odd([1, 2, 3, 4, 5]))
```

---

### **36. Program to Find Perfect Squares in a Range Where the Sum of Digits is Less Than 10**
```python
# 36.py
def is_perfect_square(n):
    return int(n**0.5)**2 == n

def sum_of_digits(n):
    return sum(int(digit) for digit in str(n))

def find_perfect_squares(start, end):
    return [x for x in range(start, end+1) if is_perfect_square(x) and sum_of_digits(x) < 10]

# Example usage
print("Perfect squares:", find_perfect_squares(1, 100))
```

---

### **37. Program to Generate Random Numbers from 1 to 20 and Append Them to a List**
```python
# 37.py
import random

random_numbers = [random.randint(1, 20) for _ in range(10)]
print("Random numbers:", random_numbers)
```

---

### **38. Program to Remove Duplicate Items from a List**
```python
# 38.py
List = [1,1,1,2,2,3,3]
final = []
duplicate = []
for n in List:
    if n not in duplicate:
        duplicate.append(n)
        final.append(n)
print("List with No Duplicates: " ,final)

```

---

### **39. Program to Create and View a Dictionary**
```python
# 39.py
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
print("Dictionary:", my_dict)
```

---

### **40. Program to Print Values of a Dictionary**
```python
# 40.py
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
print("Values:", list(my_dict.values()))
```

---

### **41. Program to Print All Keys of a Dictionary**
```python
# 41.py
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
print("Keys:", list(my_dict.keys()))
```

---

### **42. Program to Insert and Delete Elements in a Dictionary**
```python
# 42.py
my_dict = {"name": "Alice", "age": 25}
my_dict["city"] = "New York"  # Insert
del my_dict["age"]  # Delete
print("Updated dictionary:", my_dict)
```

---

### **43. Program to Sort a Dictionary by Value in Ascending and Descending Order**
```python
# 43.py
my_dict = {"a": 3, "b": 1, "c": 2}
ascending = dict(sorted(my_dict.items(), key=lambda x: x[1]))
descending = dict(sorted(my_dict.items(), key=lambda x: x[1], reverse=True))
print("Ascending:", ascending)
print("Descending:", descending)
```

---

### **44. Program to Concatenate Multiple Dictionaries**
```python
# 44.py
dict1 = {"a": 1, "b": 2}
dict2 = {"c": 3, "d": 4}
result = {**dict1, **dict2}
print("Concatenated dictionary:", result)
```

---

### **45. Program to Check if a Key Exists in a Dictionary**
```python
# 45.py
my_dict = {"name": "Alice", "age": 25}
print("Does 'name' exist?", "name" in my_dict)
```

---

### **46. Program to Merge Two Dictionaries**
```python
# 46.py
dict1 = {"a": 1, "b": 2}
dict2 = {"c": 3, "d": 4}
merged = dict1 | dict2
print("Merged dictionary:", merged)
```

---

### **47. Program to Get the Maximum and Minimum Value in a Dictionary**
```python
# 47.py
my_dict = {"a": 3, "b": 1, "c": 2}
print("Max value:", max(my_dict.values()))
print("Min value:", min(my_dict.values()))
```

---

### **48. Program to Create and View Elements of a Set**
```python
# 48.py
my_set = {1, 2, 3, 4, 5}
print("Set elements:", my_set)
```

---

### **49. Program to Add a List of Elements to a Set**
```python
# 49.py
my_set = {1, 2, 3}
my_set.update([4, 5, 6])
print("Updated set:", my_set)
```

---

### **50. Program to Update a Set with Items that Don't Exist in Another Set**
```python
# 50.py
set1 = {1, 2, 3}
set2 = {3, 4, 5}
set1.update(set2 - set1)
print("Updated set1:", set1)
```

---

### **51. Program to Find Elements Present in Either Set A or B but Not Both**
```python
# 51.py
set1 = {1, 2, 3}
set2 = {3, 4, 5}
result = set1.symmetric_difference(set2)
print("Symmetric difference:", result)
```

---

### **52. Program to Check if Two Sets Have Common Elements**
```python
# 52.py
set1 = {1, 2, 3}
set2 = {3, 4, 5}
print("Do sets have common elements?", not set1.isdisjoint(set2))
```

---

### **53. Program to Remove Items from Set1 that are Not in Set2**
```python
# 53.py
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5}
set1.intersection_update(set2)
print("Updated set1:", set1)
```

---

### **54. Function to Check if a Number is Even or Odd**
```python
# 54.py
def check_even_odd(num):
    return "Even" if num % 2 == 0 else "Odd"

# Example usage
print("10 is:", check_even_odd(10))
```

---

### **55. Function to Find the Maximum of Two Numbers**
```python
# 55.py
def max_of_two(a, b):
    return a if a > b else b

# Example usage
print("Max of 10 and 20:", max_of_two(10, 20))
```

---

### **56. Function with Keyword Arguments**
```python
# 56.py
def greet(name, message="Hello"):
    return f"{message}, {name}!"

# Example usage
print(greet("Alice", message="Hi"))
```

---

### **57. Function with Default Arguments**
```python
# 57.py
def greet(name="User"):
    return f"Hello, {name}!"

# Example usage
print(greet())
```

---

### **58. Function to Find the Factorial of a Number Using Recursion**
```python
# 58.py
def factorial(n):
    return 1 if n == 0 else n * factorial(n-1)

# Example usage
print("Factorial of 5:", factorial(5))
```

---

### **59. Function to Find the Sum of Digits of a Number Recursively**
```python
# 59.py
def sum_of_digits(n):
    return n if n < 10 else n % 10 + sum_of_digits(n // 10)

# Example usage
print("Sum of digits of 1234:", sum_of_digits(1234))
```

---

### **60. Function to Count the Number of Vowels in a String**
```python
# 60.py
def count_vowels(s):
    return sum(1 for char in s if char.lower() in "aeiou")

# Example usage
print("Number of vowels:", count_vowels("Hello World"))
```

---

### **61. Function to Greet a User with a Personalized Message**
```python
# 61.py
def greet(name):
    return f"Hello, {name}! Welcome to Python."

# Example usage
print(greet("Alice"))
```

---

### **62. Recursive Function to Print a Sequence in Reverse Order (without Using Lists)**
```python
# 62.py
def print_reverse(n):
    if n > 0:
        print(n, end=" ")
        print_reverse(n-1)

# Example usage
print_reverse(10)
```

---

### **63. Program to Store, Update, and Delete Student Records in a File**
```python
# 63.py
def add_student(file, name, age):
    with open(file, "a") as f:
        f.write(f"{name},{age}\n")

def update_student(file, name, new_age):
    with open(file, "r") as f:
        lines = f.readlines()
    with open(file, "w") as f:
        for line in lines:
            if line.split(",")[0] == name:
                f.write(f"{name},{new_age}\n")
            else:
                f.write(line)

def delete_student(file, name):
    with open(file, "r") as f:
        lines = f.readlines()
    with open(file, "w") as f:
        for line in lines:
            if line.split(",")[0] != name:
                f.write(line)

# Example usage
add_student("students.txt", "Alice", 20)
update_student("students.txt", "Alice", 21)
delete_student("students.txt", "Alice")
```

---

### **64. Program to Read and Print Content of a Text File**
```python
# 64.py
def read_file(file):
    with open(file, "r") as f:
        print(f.read())

# Example usage
read_file("example.txt")
```

---

### **65. Program to Take User Input and Write it to a New Text File**
```python
# 65.py
user_input = input("Enter text: ")
with open("output.txt", "w") as f:
    f.write(user_input)
```

---

### **66. Program to Count the Number of Words in a File and Write the Count to Another File**
```python
# 66.py
def count_words(input_file, output_file):
    with open(input_file, "r") as f:
        words = f.read().split()
    with open(output_file, "w") as f:
        f.write(f"Number of words: {len(words)}")

# Example usage
count_words("input.txt", "output.txt")
```

---

### **67. Program to Read Content of One File and Write it to Another File**
```python
# 67.py
def copy_file(source, destination):
    with open(source, "r") as src, open(destination, "w") as dest:
        dest.write(src.read())

# Example usage
copy_file("source.txt", "destination.txt")
```

---

### **68. Program to Count and Display the Number of Lines in a Text File**
```python
# 68.py
def count_lines(file):
    with open(file, "r") as f:
        lines = f.readlines()
    return len(lines)

# Example usage
print("Number of lines:", count_lines("example.txt"))
```

---

### **69. Program to Append a User-Provided String to an Existing Text File**
```python
# 69.py
user_input = input("Enter text to append: ")
with open("example.txt", "a") as f:
    f.write(user_input + "\n")
```

---

### **70. Program to Store, Update, and Delete Patient Medical Records in a File**
```python
# 70.py
def add_patient(file, name, condition):
    with open(file, "a") as f:
        f.write(f"{name},{condition}\n")

def update_patient(file, name, new_condition):
    with open(file, "r") as f:
        lines = f.readlines()
    with open(file, "w") as f:
        for line in lines:
            if line.split(",")[0] == name:
                f.write(f"{name},{new_condition}\n")
            else:
                f.write(line)

def delete_patient(file, name):
    with open(file, "r") as f:
        lines = f.readlines()
    with open(file, "w") as f:
        for line in lines:
            if line.split(",")[0] != name:
                f.write(line)

# Example usage
add_patient("patients.txt", "Alice", "Fever")
update_patient("patients.txt", "Alice", "Recovered")
delete_patient("patients.txt", "Alice")
```

---

### **71. Program to Create Two 3×3 Random Matrices and Perform Operations**
```python
# 71.py
import numpy as np

matrix1 = np.random.randint(1, 10, (3, 3))
matrix2 = np.random.randint(1, 10, (3, 3))

print("Matrix 1:\n", matrix1)
print("Matrix 2:\n", matrix2)

print("Addition:\n", matrix1 + matrix2)
print("Subtraction:\n", matrix1 - matrix2)
print("Multiplication:\n", matrix1 @ matrix2)
print("Shape:", matrix1.shape)
print("Dimensions:", matrix1.ndim)
print("Data type:", matrix1.dtype)
print("Rank:", np.linalg.matrix_rank(matrix1))
print("Flattened:", matrix1.flatten())
```

---

### **72. Program to Plot Various Charts Using Two Different Arrays**
```python
# 72.py
import matplotlib.pyplot as plt
import numpy as np

x = np.array([1, 2, 3, 4, 5])
y = np.array([10, 20, 25, 30, 40])

# Line Chart
plt.plot(x, y)
plt.title("Line Chart")
plt.show()

# Bar Chart
plt.bar(x, y)
plt.title("Bar Chart")
plt.show()

# Pie Chart
plt.pie(y, labels=x)
plt.title("Pie Chart")
plt.show()

# Scatter Plot
plt.scatter(x, y)
plt.title("Scatter Plot")
plt.show()

# Histogram
plt.hist(y)
plt.title("Histogram")
plt.show()
```
