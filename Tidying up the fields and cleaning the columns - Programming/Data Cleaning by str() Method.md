# Data Cleaning by str() Method
 
Jahnavi is going to manage the event data. She is having the data as dataframe, and her manager wants to print the data as customer name with their booking month of the event.
So help Jahnavi to print the data as customer name and the month from the date.
 
The following is the 2D format for the dataframe:   
**customer_name, address, date, eventType, cost, noOfPeople**
Here eventType is described as marriage, get together, and mehndi.  
Note: Here the date is in the format of **dd/MM/yyyy**.
Filled the data in the dataframe as the CSV file, in above format.
 
**Input Format:**
For sample data frame, see the attached  CSV  file.
 
**Output Format:**
The output is the dataframe with customer name and month of the event booking.
 
**Sample Input:**
See the attached CSV file.
 
**Sample Output:**  
cust_name  mon
0    Vikram    8
1    Sachin    4
2      Amit    9
3    Ankita   11
 
Description of the Sample Input/Output 1:
**Sample Dataframe:**

```
cust_name,addr,date,event_type,cost,no_of_people
Vikram, Hebbal, 20/08/2018, marriage, 40000, 400
Sachin, Indore, 14/04/2019, mehndi, 75000, 700
Amit, Bhopal, 24/09/2019, marriage, 20000, 600
Ankita, Delhi, 13/11/2019, mehndi, 85000, 850

 
The output is the dataframe with customer name and month of the event booking:
cust_name  mon
0    Vikram    8
1    Sachin    4
2      Amit    9
3    Ankita   11
```

```
cust_name,addr,date,event_type,cost,no_of_people
Vicky,Hebbal,8/2/2018,marriage,40000,400
Sakshi,Indore,3/9/2016,mehndi,75000,700
Amit,Bhopal,1/3/2012,marriage,20000,600
Ankita,Delhi,24/12/2019,mehndi,85000,850
Vikas,Hebbal,3/11/2019,marriage,40000,400
Santosh,Indore,29/10/2014,mehndi,75000,700

The output is the dataframe with customer name and month of the event booking:

cust_name mon
0 Vicky 8
1 Sakshi 3
2 Amit 1
3 Ankita 12
4 Vikas 3
5 Santosh 10
```

### Solution:
```Python
import pandas as pd

df = pd.read_csv("dataFrame3.csv")

df['mon'] = pd.to_datetime(df['date']).dt.month

print(df[["cust_name", "mon"]])
```
