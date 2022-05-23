# Problem1 Profit/Loss

# PROBLEM1

## Profit/Loss

Ramesh is self-employed. it's been years after setting his business. With all the hardships he brought his business into the track. He got a thought to analyze his graph of progress from last year to the current year.

He has a list of data in which he has recorded the profit of his business of past year (Month by Month) and similarly the current year's. But unaware of any software he had to do it manually which was a tedious work. He asks Suresh, a Software Engineer to help him in this. Fortunately, Suresh was working on data science and thought he could easily help him.

Assume yourself to be in Suresh's position and had to help Ramesh in tracking his growth from last year to current year. Given the data set of profit gained in every month for 2 years, calculate if he has gained profit over the year.

**Input Format:**

First, 12 inputs corresponding to the profit gained in each month of the previous Year.
Next input consists of an integer 'n' indicating the current month of the current year.
Next n inputs consist of the profits gained in 'n' months of the current year.

**Output format:**

The Output contains 2 columns Month and Profit/Loss. The negative values under the Profit/Loss column are considered as Loss and Positive values are considered as Profit.
**Print "Invalid Input". If n value is <=0 and >12.**
Use this month format to display Month **['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sept','Oct','Nov','Dec'].**
Refer sample input and Output for format specifications.

Sample Input-Output 1:

Enter previous year monthly turnover
25000

12000

10000

15000

2700

45000

21000

32000

150200

25000

250000

32000

Enter the number of months covered in present year

O

Invalid Input

Sample Input -Output 2:

Enter previous year monthly turnover

20000

12000

23000

45000

65000

152039

48780

35760

2000

10000

15000

25000

Enter the number of months covered in present year

4

55000

15000

65000

250250

Positive values corresponds to Profit were as negative values corresponds to Loss

Month Profit/Loss

0 Jan 35000

1 Feb 3000

2 Mar 42000

3 Apr 205250

Additional Sample TestCases

Sample Input and Output 1 :

Enter previous year monthly turnover

25000

12000

10000

15000

2700

45000

21000

32000

150200

25000

250000

32000

Enter the number of months covered in present year

0

Invalid Input

```
def main():
    previousYear = []
    currentYear = []
    print("Enter previous year monthly turnover")
    for i in range(12):
        previousYear.append(int(input()))
    print("Enter the number of months covered in present year")
    input_month = int(input())
    if input_month <= 0 or input_month > 12:
        print("Invalid Input")
        return
    else:
        for i in range(input_month):
            currentYear.append(int(input()))
        print("Positive values corresponds to Profit were as negative values corresponds to Loss")
        print("  Month ", " Profit/Loss")

        for i in range(input_month):
            print(" ",i, "   ", f"{['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sept','Oct','Nov','Dec'][i]}","   ", currentYear[i]-previousYear[i])

main()
```
