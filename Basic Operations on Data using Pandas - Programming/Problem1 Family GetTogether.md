# Problem1 Family GetTogether

# Family GetTogether

**Input:**

Enter the number row and columns

2

2

Enter the element to be inserted

1

2

3

4

**Output:**

Array before Flattening

1 2
3 4

Array After Flattening

1 2 3 4

```
import numpy as np
print("Enter the number row and columns")
row = int(input())
column = int(input())
print("Enter the element to be inserted")
matrix = []
for i in range(row):
    matrix.append([])
    for j in range(column):
        matrix[i].append(int(input()))
print("Array before Flattening")
for a in matrix:
    print(*a)
print("Array After Flattening")
b = np.array(matrix)
print(*b.flatten())
```
