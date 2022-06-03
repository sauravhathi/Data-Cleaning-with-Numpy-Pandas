# <p align="center">Fun Game - 1</p>
 
Sita works as an event organizer. Since her young age, she was always interested in organizing the kitty parties and she organizes some fun events for her customers as well. 
 
This time she has planned an interesting game and the game is as follows.
Sita has a data set of numbers in the form of a square matrix. And the contestants are made to sit in the same matrix form. Each of the contestants will announce the lucky number.
 
One more person is allocated to call one among the four following options. The options are **1. Next 2.Previous and 3. Diagonal 4. Exit**
 
If next option is called, then the data set which Sita has will be added to the corresponding lucky numbers of the contestants. 
 
If previous option is called, then the data set which Sita has will be subtracted from corresponding lucky numbers of the contestants.
 
If the Diagonal option is called, then the contestants who are sitting in the diagonal positions will only remain. 
 
If the Exit option is called then the game ends at that point.
But Sita is a bit worried as she has to dynamically calculate the next, previous and diagonal data sets. Let’s help Sita by writing code.
 
Given a number ‘n’, write a code to create a data set in the form of ‘nXn’ matrix.
Note: The number of contestants playing the **game** at a time should be equal to n. The next input should be one among the 4 options (1/2/3/4).
Display what will be the data set for the corresponding options. And **display invalid input if the order of the seating arrangement is negative.**
 
**Input Format:**
The first line of the input consists of an integer corresponding to the Order of the data set (matrix).
The Second line of the input corresponds to the starting seat number.
The next inputs correspond to be the **choice among 4 options (1/2/3/4).**
 
**Output Format:**
Refer the Sample input and output for format specifications.
 
**Sample Input - Output:**

```python
Enter the order of seating arrangement
4
Enter the starting seat  number
20
20 21 22 23
24 25 26 27
28 29 30 31
32 33 34 35
Enter your choice
1)next
2)previous
3)Diagonal elements
4)Exit
1
36 37 38 39
40 41 42 43
44 45 46 47
48 49 50 51
Enter your choice
1)next
2)previous
3)Diagonal elements
4)Exit
2
20 21 22 23
24 25 26 27
28 29 30 31
32 33 34 35
Enter your choice
1)next
2)previous
3)Diagonal elements
4)Exit
3
20 0 0 0
0 25 0 0
0 0 30 0
0 0 0 35
Enter your choice
1)next
2)previous
3)Diagonal elements
4)Exit
4
```

**Additional Sample TestCases
Sample Input and Output 1 :** 
```python
Enter the order of seating arrangement
4
Enter the starting seat number20
20 21 22 23
24 25 26 27
28 29 30 31
32 33 34 35
Enter your choice
1)next
2)previous
3)Diagonal elements
4)Exit
1
36 37 38 39
40 41 42 43
44 45 46 47
48 49 50 51
Enter your choice
1)next
2)previous
3)Diagonal elements
4)Exit
2
20 21 22 23
24 25 26 27
28 29 30 31
32 33 34 35
Enter your choice
1)next
2)previous
3)Diagonal elements
4)Exit
3
20 0 0 0
0 25 0 0
0 0 30 0
0 0 0 35
Enter your choice
1)next
2)previous
3)Diagonal elements
4)Exit
4
```

```python
Input: 5
25
3
4

Enter the order of seating arrangement
Enter the starting seat number
25 26 27 28 29
30 31 32 33 34
35 36 37 38 39
40 41 42 43 44
45 46 47 48 49
Enter your choice
1)next
2)previous
3)Diagonal elements
4)Exit
25 0 0 0 0
0 31 0 0 0
0 0 37 0 0
0 0 0 43 0
0 0 0 0 49
```

```python
import numpy as np

def main(stating_seat_number):
    choice = int(input("\nEnter your choice\n 1)next\n 2)previous\n 3)Diagonal elements\n 4)Exit\n"))
    if choice == 1:
        next_stating_seat_number = stating_seat_number+n*n
        x = np.arange(start=next_stating_seat_number,stop=next_stating_seat_number+n*n, step=1)
        x.shape = (n, n)
        for i in range(n):
            for j in range(n):
                print(x[i][j], end=" ")
            print("\n", end="")
        main(next_stating_seat_number)

    elif choice == 2:
        temp = (int)(stating_seat_number/2)
        print("\n", end="")
        x = np.arange(start=temp, stop=temp+n*n, step=1)
        x.shape = (n, n)
        # print(x)
        for i in range(n):
            for j in range(n):
                print(x[i][j], end="")
            print("\n", end="")
        main(temp)

    elif choice == 3:
        dg = stating_seat_number - n*n
        x = np.arange(start=stating_seat_number,stop=stating_seat_number+n*n, step=1)
        x.shape = (n, n)
        # print(np.diag(np.diag(x)))
        for i in range(n):
            for j in range(n):
                if i == j:
                    print(x[i][j], end=" ")
                else:
                    print("0", end=" ")
            print("\n", end="")
        main(dg)

    elif choice == 4:
        exit()

n = int(input("Enter the order of seating arrangement"))
if n < 0:
    print("\nInvalid input")
    
else:
    stating_seat_number = int(input("\nEnter the starting seat number"))
    print("\n", end="")
    x = np.arange(start=stating_seat_number, stop=stating_seat_number+n*n, step=1)
    x.shape = (n,n)
    for i in range(n):
        for j in range(n):
            print(x[i][j], end=" ")
        print("\n", end="")
    main(stating_seat_number)
```

Happy Coding
