# Problem2 Splitting the Dataframe

# Splitting the Dataframe

* * *
**Supporting Documents:**

dataFrame1.csv

cust_name,addr,date,event_type,cost,no_of_people
Dilip,hebbal,27/12/2018,marriage,40000,400
Prakash,indore,18/05/2014,mehndi,70000,700
Ajith,bhopal,20/01/2020,marriage,20000,200
Akshay,kanpur,10/11/2017,get together,10000,300
Varun,Delhi,21/09/2020,marriage,20000,200
Sunil,Agra,19/07/2017,get together,35000,300

* * *

```
import pandas as pd

df = pd.read_csv('dataFrame1(1).csv')

df['date'] = pd.to_datetime(df['date'], format='%d/%m/%Y').dt.strftime('%m')
df['date'] = df['date'].astype(int)

print("Bookings on or Before June:")
before_june = df[df['date'] <= 6]

print(before_june[['cust_name', 'date', 'cost']].to_string(index=False))

print("Total number of bookings on or Before June:")
print(len(before_june))

print("Total booking cost on or Before June:")
print(before_june['cost'].sum())

print("Bookings After June:")
after_june = df[df['date'] > 6]

print(after_june[['cust_name', 'date', 'cost']].to_string(index=False))

print("Total number of bookings After June:")
print(len(after_june))

print("Total booking cost After June:")
print(after_june['cost'].sum())

```

**Output**: In Tabulated form
```
Bookings on or Before June:
+----+-------------+--------+--------+--------------+--------+----------------+
|    | cust_name   | addr   |   date | event_type   |   cost |   no_of_people |
|----+-------------+--------+--------+--------------+--------+----------------|
|  1 | Prakash     | indore |      5 | mehndi       |  70000 |            700 |
|  2 | Ajith       | bhopal |      1 | marriage     |  20000 |            200 |
+----+-------------+--------+--------+--------------+--------+----------------+
Total number of bookings on or Before June:
2
Total booking cost on or Before June:
90000
Bookings After June:
+----+-------------+--------+--------+--------------+--------+----------------+
|    | cust_name   | addr   |   date | event_type   |   cost |   no_of_people |
|----+-------------+--------+--------+--------------+--------+----------------|
|  0 | Dilip       | hebbal |     12 | marriage     |  40000 |            400 |
|  3 | Akshay      | kanpur |     11 | get together |  10000 |            300 |
|  4 | Varun       | Delhi  |      9 | marriage     |  20000 |            200 |
|  5 | Sunil       | Agra   |      7 | get together |  35000 |            300 |
+----+-------------+--------+--------+--------------+--------+----------------+
Total number of bookings After June:
4
Total booking cost After June:
105000

```

**Output**
```
Bookings on or Before June:
cust_name  date  cost
  Prakash     5 70000
    Ajith     1 20000
Total number of bookings on or Before June:
2
Total booking cost on or Before June:
90000
Bookings After June:
cust_name  date  cost
    Dilip    12 40000
   Akshay    11 10000
    Varun     9 20000
    Sunil     7 35000
Total number of bookings After June:
4
Total booking cost After June:
105000
```