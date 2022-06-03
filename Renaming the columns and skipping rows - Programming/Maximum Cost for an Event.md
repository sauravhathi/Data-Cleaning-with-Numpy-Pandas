# Maximum Cost for an Event

Aakash is going to manage the event data . He is having the data as dataframe, and his manager is requesting him to find the maximum cost for an event.
So help Aakash to find the maximum cost for an event, by pandas library of python.

The following is the 2D format for the dataframe:
customer_name, address, date, eventType, cost, noOfPeople
Here eventType is described as marriage, get together, and mehndi.

Filled the data in the dataframe as the CSV file, in above format.

**Input Format:**
For sample data frame, see the attached CSV file.

**Output Format:**
The output is the integer value as maximum cost for an event.

**Sample Input:**
```python
cust_name,addr,date,event_type,cost,no_of_people
vikram,hebbal,04/20/2018,marriage,40000,200
sachin,indore,"09,10,2019",mehndi,70000,700
amit,bhopal,08/23/2018,marriage,20000,400
vikram,kanpur,06/21/2019,get together,30000,300
```


**Sample Output:**
70000

**Sample Input:**
``python
cust_name addr date event_type cost no_of_people
vikram hebbal 4/20/2018 marriage 20000 200
sachin indore 09,10,2019 mehndi 70000 700
amit bhopal 8/23/2018 marriage 20000 400
vikram kanpur 6/21/2019 get together 200000 300
```

**Sample Output:**
200000

### Solution:

```
import pandas as pd

df = pd.read_csv("dataFrame1.csv", error_bad_lines=False)
print(df["cost"].max())
```
