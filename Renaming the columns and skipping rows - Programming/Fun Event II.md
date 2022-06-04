# <p align="center">Fun Event II</p>
 
As the part of Farewell of an employee, Gowri. The HR team organized a fun event. All the employees who came for the event were made to sit in the  'r' rows and 'c' columns.

At the end of the events, Gowri decided to distribute the prize money to all the employees who had gathered for the event. The prize money was distributed by taking the difference between two aged person and young person and so many hundreds of rupees were distributed to the whole row employees.
Write a program which helps to find out the difference between **aged(max)** and **young(min)** person in each row.
 
**Input format:**
The first line of the input consists of an integer which corresponds to a number of rows in the event hall.
The second line of the input consists of an integer which corresponds to a number of columns in the event hall.
Next **r*c** elements consist of an individual age of each employee according to their seating arrangement.
 
**Output format:**
The output consists of the difference between aged(max) and young(min) person wrt corresponding row.
 
**Sample Input-Output:**

```python
Enter the number rows in the Event Hall
5
Enter the number columns in the Event Hall
5
Enter the age og each employee in their seating order
21,22,32,41,23
27,31,55,31,22
33,36,55,23,56
29,25,26,38,42
55,23,52,41,35
Max - Min in 1 row is 20
Max - Min in 2 row is 33
Max - Min in 3 row is 33
Max - Min in 4 row is 17
Max - Min in 5 row is 32
```
 
```python
Additional Sample TestCases
Sample Input and Output 1 :
Enter the number rows in the Event Hall
5
Enter the number columns in the Event Hall
5
Enter the age og each employee in their seating order
21,22,32,41,23 
27,31,55,31,22 
33,36,55,23,56 
29,25,26,38,42 
55,23,52,41,35  
Max - Min in 1 row is 20
Max - Min in 2 row is 33
Max - Min in 3 row is 33
Max - Min in 4 row is 17
Max - Min in 5 row is 32
```

```
Input: 2
4
21,34,42,31
31,31,54,25

Enter the number rows in the Event Hall
Enter the number columns in the Event Hall
Enter the age of each employee in their seating order
Max - Min in 1 row is 21
Max - Min in 2 row is 29
```

**Solution:**

```python
import pandas as pd
import numpy as np

print("Enter the number rows in the Event Hall")
r = int(input())

print("Enter the number columns in the Event Hall")
c = int(input())

print("Enter the age og each employee in their seating order")
df = pd.DataFrame(np.zeros((r,c)))
temp={}

for i in range(r):
    temp[i] = (input().split(','))

df = pd.DataFrame(temp)

# print(df)

for i in range(r):
    df[i] = df[i].astype(int)
    print("Max - Min in",i+1,"row is", max(df[i])-min(df[i]))
```
