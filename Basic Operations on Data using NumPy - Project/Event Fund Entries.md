# <p align="center">Event Fund Entries</p>
 

"Band Baja Barath" is a famous Event organizing company in the town, Sunil who had just finished his MBA wanted to apply for the Event Manager position in the same organization. In order to check the employee's efficiency and performance, they provided the event data for the corresponding month asking him to perform some simple data management over the given set of data.

Before performing any operation it is very important to arrange the data in the dataset. The key elements they wanted to check were in what dimension the candidate is arranging the data, a number of elements present in the dataset and range, he has arranged the data in. So help by building an auto-evaluating tool which displays the number of elements present, in what dimension is it arranged.

Write a program to receive n+1 data from the user and add them to the dataset and present the data using ndim,size,axes...

**Input Format:**

The first line of the input corresponds to the number of elements to be inserted into the data set(Integer).

Next, n lines correspond to the element present inside the data set.

**Output Format:**

The output will first display elements present in the dataset 

Followed by the dimension, the number of elements present and indexing range of the data set.

If no elements are present print **"Dataset is empty"**.

**Sample Input - Output 1:**
```python
Enter number of elements
0
Enter the elements
Dataset is empty
```
 

**Sample Input - Output 2:**
```python
Enter number of elements
3
Enter the elements
12450
15000
24000
Elements in the dataset
0    12450
1    15000
2    24000
dtype: int64
Dataset is with 1 dimension data
Number of elements in the dataset is 3
RangeIndex(start=0, stop=3, step=1)
``` 

**Additional Sample TestCases
Sample Input and Output 1 :**

```python
Enter number of elements
3
Enter the elements
12450
15000
24000
Elements in the dataset
0    12450
1    15000
2    24000
dtype: int64
Dataset is with 1 dimension data
Number of elements in the dataset is 3
RangeIndex(start=0, stop=3, step=1)
```

```python
Input: 3
"Marraige"
"Birthday Celebration"
"Family Gettogether"

Enter number of elements
Enter the elements
Elements in the dataset
0 Marraige
1 Birthday Celebration
2 Family Gettogether
dtype: object
Dataset is with 1 dimension data
Number of elements in the dataset is 3
RangeIndex(start=0, stop=3, step=1)
```

```python
Input: 5
99999.99
11000.00
2500
21035
21094

Enter number of elements
Enter the elements
Elements in the dataset
0 99999.99
1 11000.00
2 2500.00
3 21035.00
4 21094.00
dtype: float64
Dataset is with 1 dimension data
Number of elements in the dataset is 5
RangeIndex(start=0, stop=5, step=1)
```

**Solution:**

```python
```
