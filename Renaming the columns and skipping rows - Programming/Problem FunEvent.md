# Problem FunEvent

# PROBLEM

## Fun Event

As the part of Farewell of a colleague Gowri, all employees decided to organize a fun event. All the employees who came for the event were made to register a day before. A list was formed of all the registered employee according to their ages which were entered one after the other. (in the form of 1-D Array).

The organizers decided to make the seating arrangements in rows and columns. Given the list of the registered employees (in 1D array) the seats for them had to be arranged in rows and columns (in 2D array). Write a code to help the organizers to make a proper seating arrangement.

Hint: For seating arrangement consider the total number of registration and the maximum divisor of that number.

i.e newly formed 2D array's number of the rows=Quotient and columns= maximum divisor are as follows.

### Input format:

Input Consists of Age list of all the employee registered.

### Output format:

The output will be a 2D arrangement of an employee's age.

### Sample Input-Output:

```
Enter the age of employees registered

21,31,42,22,29,45,36,25
Number of rows 2
Number of columns 4

Employees are made to sit in the following order

21 31 42 22

29 45 36 25
```

**Additional Sample TestCases
Sample Input and Output 1 :**

```
Enter the age of employees registered
21,31,42,22,29,45,36,25
Number of rows 2
Number of columns 4
Employees are made to sit in the following order
21 31 42 22
29 45 36 25
```

### Solution:

```Python
arr = {}
print("Enter the age of employees registered")

input_list = input().split(',')
for i in range(0, len(input_list)):
    arr[i] = int(input_list[i])

maxDivisor = len(arr)-1
for maxDivisor in range(len(arr)-1, 0, -1):
    if len(arr) % maxDivisor == 0:
        break
print("Number of rows", len(arr)//maxDivisor, "\nNumber of columns",
      maxDivisor, "\nEmployees are made to sit in the following order")
for k in range(0, len(arr)//maxDivisor):
    for j in range(0, maxDivisor):
        print(arr[k*maxDivisor+j], end=" ")
    print()
```
HappyCoding