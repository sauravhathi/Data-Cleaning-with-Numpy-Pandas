Column Indexing
 
Praveen, MBA student decided to begin a business on his own in event management. He also set a good pace very soon but lately, it was difficult for him to keep things in track and note which is the upcoming event as the event list was not maintained. Hence Praveen wanted to build an application in which on entering the column name the indexing should be done using those column values. which could help him sort events faster.
 Write a program to input the column name so that all data stored in the dataset is display along with column selected as the index.
Note:Column name in the dataset should be as follows
( 'Sl No','EventName','EventManager','NoOfDates','StartDate','EndDate','HallName','HallAddress','HallPricePerDay','TotalCost' )

**Input Format:**

The first line of the input consists of the number of rows of data present in the dataset.
Next, n lines correspond to the data be added to the dataset.
The last line of the input would consist of a string which corresponds to the column name in the dataset.

**Output Format:**

Based on the last input(column name)data from the dataset is displayed.
Refer sample input-output for better understanding.
(All the in bold corresponds to input and rest corresponds to the output)

**Sample Input-Output:**
```python
Enter the number of rows of data to be added to the dataset
8
Enter the data to be added to the dataset
1 ,Marriage ,krishnanand,2,12-08-2005,13-08-2005,krishna mansion,Krishna Mansion  Krishnalaya Shringeri,60000,120000
2 ,Birthday Celebration,Akshay,1,14-08-2005,14-08-2005,Akshayalaya,Akshayalaya  Akshaya Dama Yogendra Nagar Shimoga,35000,35000
3 ,House Warming,sunil,1,21-10-2005,21-10-2005,Sugamya Corner,Sugamya corner  Vijaya nagar Mysore,50000,50000
4 ,Naming Ceremony,Surya,1,10-11-2005,10-11-2005,Suryodaya comforts,Suryodaya comforts Srirampura,20000,20000
5 ,Promossion Celebration,Aliya,1,15-11-2005,15-11-2005,Kabule convention hall,Kabule convention hall Bangalore,20000,20000
6 ,New Year Celebration,Chandan,2,31-12-2005,01-12-2005,Chinnaswammy stadium,Bangalore,12000,24000
7 ,Chrismas Celebration,Collin,2,24-12-2005,25-12-2005,Saint Philominas chruch,Saint Philominas chruch Mysore,25000,50000
8 ,Project outing,Santhosh,2,29-11-2005,30-11-2005,Mysore Palace Resort,Mysore Palace Resort Mysore,15000,30000
Enter the column name 
EventName

Marriage             
Birthday Celebration    
House Warming          
Naming Ceremony         
Promossion Celebration   
New Year Celebration    
Chrismas Celebration     
Project outing          
 
 Name: EventName, dtype: object
 ```
 
**Additional Sample TestCases
Sample Input and Output 1 :**
```python
Enter the number of rows of data to be added to the dataset
1
Enter the data to be added to the dataset
8 ,Project outing,Santhosh,2,29-11-2005,30-11-2005,Mysore Palace Resort,Mysore Palace Resort Mysore,15000,30000
Enter the column nameHallAddress
                            Sl No    ...    TotalCost
HallAddress                          ...             
Mysore Palace Resort Mysore    8     ...        30000

[1 rows x 9 columns]
```
**Sample Input and Output 2 :**
```python
8
Enter the number of rows of data to be added to the dataset
Enter the data to be added to the dataset
1 ,Marriage ,krishnanand,2,12-08-2005,13-08-2005,krishna mansion,Krishna Mansion  Krishnalaya Shringeri,60000,120000
2 ,Birthday Celebration,Akshay,1,14-08-2005,14-08-2005,Akshayalaya,Akshayalaya  Akshaya Dama Yogendra Nagar Shimoga,35000,35000
3 ,House Warming,sunil,1,21-10-2005,21-10-2005,Sugamya Corner,Sugamya corner  Vijaya nagar Mysore,50000,50000
4 ,Naming Ceremony,Surya,1,10-11-2005,10-11-2005,Suryodaya comforts,Suryodaya comforts Srirampura,20000,20000
5 ,Promossion Celebration,Aliya,1,15-11-2005,15-11-2005,Kabule convention hall,Kabule convention hall Bangalore,20000,20000
6 ,New Year Celebration,Chandan,2,31-12-2005,01-12-2005,Chinnaswammy stadium,Bangalore,12000,24000
7 ,Chrismas Celebration,Collin,2,24-12-2005,25-12-2005,Saint Philominas chruch,Saint Philominas chruch Mysore,25000,50000
8 ,Project outing,Santhosh,2,29-11-2005,30-11-2005,Mysore Palace Resort,Mysore Palace Resort Mysore,15000,30000
Enter the column name
EventName
                       Sl No EventManager    ...    HallPricePerDay TotalCost
EventName                                    ...                             
Marriage                  1   krishnanand    ...              60000    120000
Birthday Celebration      2        Akshay    ...              35000     35000
House Warming             3         sunil    ...              50000     50000
Naming Ceremony           4         Surya    ...              20000     20000
Promossion Celebration    5         Aliya    ...              20000     20000
New Year Celebration      6       Chandan    ...              12000     24000
Chrismas Celebration      7        Collin    ...              25000     50000
Project outing            8      Santhosh    ...              15000     30000

[8 rows x 9 columns]
```
**Solution:**
```python
import pandas as pd

n = int(input("Enter the number of rows of data to be added to the dataset\n"))
df = pd.DataFrame(columns=['Sl No','EventName','EventManager','NoOfDates','StartDate','EndDate','HallName','HallAddress','HallPricePerDay','TotalCost'])

print("Enter the data to be added to the dataset")
for i in range(n):
    data = input().split(',')
    df.loc[i] = data

column_name = input("Enter the column name\n")
print("   ",df[column_name].to_string(index=False))
print("Name:",column_name,",","dtype:",df[column_name].dtype)
```
Happy Coding
