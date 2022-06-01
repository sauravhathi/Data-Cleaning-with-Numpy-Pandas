# Event management System 5

# Event management System – V

Sunil the event Manager wanted to send the list of events registered\***\* in the corresponding month to the auditor for IT filing. But the problem was once the CSV file is received the data in it would be only in the string format. Hence he was tensed as the calculation would go wrong in some of the fields(**TotalCost, Number of Dates\*\*,etc...).

Write a program to read the data by retaining the data type of the Column**[NoOfDates,TotalCost]** along with the data type in the dataset.

Input Format:
Create a CSV file containing the data set of 10 rows and 10 columns. Along with the CSV file, change the columns **‘NoOfDates’** and **‘TotalCost’**

NOTE:
CSV File contains the comma seperated values as shown below.
**[SlNo,EventName,EventManager,NoOfDates,StartDate,EndDate,HallName,HallAddress,HallPricePerDay,TotalCost]**

Output Format:
The Output should display the data after changing the data type of the columns **‘NoOfDates’ ‘TotalCost’** .

### Sample Input 1:

**Event_Management_system.csv**

```Sl_No,EventName,EventManager,NoOfDates,StartDate,EndDate,Expected Audience,HallName,HallAddress,HallPricePerDay,TotalCost
1,,krishnanand,2,12-08-2005,13-08-2005,20000,krishna mansion,"Krishna Mansion ,Krishnalaya,Shringeri",60000,120000
2,Birthday Celebration,Akshay,1,14-08-2005,14-08-2005,,Akshayalaya,"Akshayalaya, Akshaya Dama,Yogendra Nagar,Shimoga",35000,35000
3,House Warming,sunil,1,21-10-2005,21-10-2005,1000,Sugamya Corner,"sugamya corner ,Vijaya nagar,Mysore",50000,50000
4,Naming Ceremony,Surya,1,10-11-2005,10-11-2005,1500,Suryodaya comforts,"Suryodaya comforts,Srirampura",20000,20000
5,Promossion Celebration,Aliya,1,15-11-2005,15-11-2005,250,Kabule convention hall,"Nr Mohalla,Mysore",20000,20000
6,New Year Celebration,Chandan v           ,,31-12-2005,01-12-2005,700,Chinnaswammy stadium,Bangalore,12000,24000
7,Chrismas Celebration,Collin,2,24-12-2005,25-12-2005,1500,Saint Philominas chruch,Mysore,25000,50000
8,Project outing,Yaradru,2,,30-11-2005,25,Lalth Mahal Palace,Mysore,15000,30000
9,Birthday Celebration,Akshay,1,14-08-2005,14-08-2005,10000,Akshayalaya,"Akshayalaya, Akshaya Dama,Yogendra Nagar,Shimoga",35000,35000
10,Reception,krishnanand,2,12-08-2005,13-08-2005,25000,krishna mansion,"Krishna Mansion ,Krishnalaya,Shringeri",60000,120000
11,Marraige,krishnanand,1,15-08-2005,16-08-2005,25000,krishna mansion,"Krishna Mansion ,Krishnalaya,Shringeri",60000,60000
```

### Sample Output 1:

```
NoOfDates TotalCost
0 2.0 120000.0
1 1.0 35000.0
2 1.0 50000.0
3 1.0 20000.0
4 1.0 20000.0
5 NaN 24000.0
6 2.0 50000.0
7 2.0 30000.0
8 1.0 35000.0
9 2.0 120000.0
10 1.0 60000.0
```

### Solution:

```Python
import pandas as pd

df = pd.read_csv("Event_Management_system5.csv")

df['NoOfDates'] = df['NoOfDates'].astype(float).fillna('NaN')
df['TotalCost'] = df['TotalCost'].astype(float)

print(df[['NoOfDates', 'TotalCost']])
```

HaPPy CoDing
