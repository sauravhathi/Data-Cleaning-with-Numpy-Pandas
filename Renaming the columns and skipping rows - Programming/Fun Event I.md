# <p align="center">Fun Event I</p>

As the part of Farewell of an employee, Gowri. The HR team organized a fun event. All the employees who came for the event were made to sit in the 2-D array format with 'r' rows and 'c' columns.
 

The game was to find the most aged and the youngest person in each row. Given the seating arrangement of all the employees Write a program which helps to find out aged(max) and young(min) person in each row.

 

Input format:

The first line of the input consists of an integer which corresponds to the number of rows.

The second line of the input consists of an integer which corresponds to the number of columns.

Next r*c elements consist of an individual age of each employee according to their seating arrangement.

 

**Output format:**

The output consists of **Aged(max)** and **young(min)** person wrt corresponding row.

 

**Sample Input-Output:**
```python
Enter the number rows

5

Enter the number columns

5

Enter the age of each employee in their seating order

21,22,32,41,23

27,31,55,31,22

33,36,55,23,56

29,25,26,38,42

55,23,52,41,35

Max and Min Aged person in 1 row are 41 and 21

Max and Min Aged person in 2 row are 55 and 22

Max and Min Aged person in 3 row are 56 and 23

Max and Min Aged person in 4 row are 42 and 25

Max and Min Aged person in 5 row are 55 and 23
```

```python
Additional Sample TestCases
Sample Input and Output 1 :
Enter the number rows in the Event Hall
4
Enter the number columns in the Event Hall
2
Enter the age og each employee in their seating order
25,31
24,55
23,35
56,23
Max and Min Aged person in 1 row are 31 and 25
Max and Min Aged person in 2 row are 55 and 24
Max and Min Aged person in 3 row are 35 and 23
Max and Min Aged person in 4 row are 56 and 23
```

**Solution:**

```python
import pandas as pd
import numpy as np

print("Enter the number rows in the Event Hall")
r = int(input())

print("Enter the number columns in the Event Hall")
c = int(input())

print("Enter the age of each employee in their seating order")

df = pd.DataFrame(np.zeros((r,c)))
temp={}

for i in range(r):
    temp[i] = (input().split(','))
    
df = pd.DataFrame(temp)

for i in range(r):
    df[i] = df[i].astype(int)
    print("Max and Min Aged person in",i+1,"row are",df[i].max(),"and",df[i].min())
```
