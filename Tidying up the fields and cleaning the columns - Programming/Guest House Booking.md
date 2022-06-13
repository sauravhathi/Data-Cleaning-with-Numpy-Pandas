Guest House Booking: “Sugamya Corner” a very well known Guesthouse initially the booking count was quite less as the day progressed the number of guests started increasing it was difficult to balance them and calculate the account related things required by auditing was difficult so they decided to build a system which receives booking details of all the guess and stores it in a dataset which makes it easy to access and for each calculation.
Write a program to accept the data of the guest bookings for the guest house and display them with the column name as [“GuestName”, “PhoneNumber”, “EmailId”, “Address”, “Age”, “NoOfDays”, “CostPerDay”] for better understanding accessing.


 
Guest House Booking using Pandas
Input-Output Format:

The first line of the input corresponds to the number of bookings.


 
The Next n line corresponds to booking details(GuestName, PhoneNumber,  EmailId, Address, Age, NoOfDays, CostPerDay) of the guest.

Refer Sample Input-output for better understanding.

Sample Input-Output:

Enter the number of bookings
3
Sunil,7869054132,sunil21@gmail.com,Srirampura,28,7,500.00
Akshay,8901234567,akshay@amphisoft.co.in,Vijay Nagar,27,1,650.00
Krishnanand,9876543210,krishnanand@amphisoft.co.in,Ramakrishna Nagar,28,2,500.00
+—+————-+————-+—————————–+——————-+—–+———-+————+
|   |  GuestName  | PhoneNumber |           EmailId           |      Address      | Age | NoOfDays | CostPerDay |
+—+————-+————-+—————————–+——————-+—–+———-+————+
| 0 |    Sunil    |  7869054132 |      sunil21@gmail.com      |     Srirampura    |  28 |    7     |   500   |
| 1 |    Akshay   |  8901234567 |    akshay@amphisoft.co.in   |    Vijay Nagar    |  27 |    1     |   650   |
| 2 | Krishnanand |  9876543210 | krishnanand@amphisoft.co.in | Ramakrishna Nagar |  28 |    2     |   500   |
+—+————-+————-+—————————–+——————-+—–+———-+————+
 


 
Additional Sample TestCases
Sample Input and Output 1 :

Enter the number of bookings
3
Sunil,7869054132,sunil21@gmail.com,Srirampura,28,7,500
Akshay,8901234567,akshay@amphisoft.co.in,Vijay Nagar,27,1,650
Krishnanand,9876543210,krishnanand@amphisoft.co.in,Ramakrishna Nagar,28,2,500
+---+-------------+-------------+-----------------------------+-------------------+-----+----------+------------+
|   |  GuestName  | PhoneNumber |           EmailId           |      Address      | Age | NoOfDays | CostPerDay |
+---+-------------+-------------+-----------------------------+-------------------+-----+----------+------------+
| 0 |    Sunil    |  7869054132 |      sunil21@gmail.com      |     Srirampura    |  28 |    7     |   500.00   |
| 1 |    Akshay   |  8901234567 |    akshay@amphisoft.co.in   |    Vijay Nagar    |  27 |    1     |   650.00   |
| 2 | Krishnanand |  9876543210 | krishnanand@amphisoft.co.in | Ramakrishna Nagar |  28 |    2     |   500.00   |
+---+-------------+-------------+-----------------------------+-------------------+-----+----------+------------+
Sample Input and Output 2 :

Enter the number of bookings
5
Mahadev,6789098760,mahadev@gmail.com,25,7,500
Prasanna,7890345612,prasannaGowda@gmail.com,19,365,1000
Sunil,7869054132,sunil21@gmail.com,Srirampura,28,7,500
Akshay,8901234567,akshay@amphisoft.co.in,Vijay Nagar,27,1,650
Krishnanand,9876543210,krishnanand@amphisoft.co.in,Ramakrishna Nagar,28,2,500
+---+-------------+-------------+-----------------------------+-------------------+-----+----------+------------+
|   |  GuestName  | PhoneNumber |           EmailId           |      Address      | Age | NoOfDays | CostPerDay |
+---+-------------+-------------+-----------------------------+-------------------+-----+----------+------------+
| 0 |   Mahadev   |  6789098760 |      mahadev@gmail.com      |         25        |  7  |  500.00  |    None    |
| 1 |   Prasanna  |  7890345612 |   prasannaGowda@gmail.com   |         19        | 365 | 1000.00  |    None    |
| 2 |    Sunil    |  7869054132 |      sunil21@gmail.com      |     Srirampura    |  28 |    7     |   500.00   |
| 3 |    Akshay   |  8901234567 |    akshay@amphisoft.co.in   |    Vijay Nagar    |  27 |    1     |   650.00   |
| 4 | Krishnanand |  9876543210 | krishnanand@amphisoft.co.in | Ramakrishna Nagar |  28 |    2     |   500.00   |
+---+-------------+-------------+-----------------------------+-------------------+-----+----------+------------+

Input: 3
Sunil,7869054132,sunil21@gmail.com,Srirampura,28,7,500.00
Akshay,8901234567,akshay@amphisoft.co.in,Vijay Nagar,27,1,650.00
Krishnanand,9876543210,krishnanand@amphisoft.co.in,Ramakrishna Nagar,28,2,500.00

Enter the number of bookings
+----+-------------+---------------+-----------------------------+-------------------+-------+------------+--------------+
|    | GuestName   |   PhoneNumber | EmailId                     | Address           |   Age |   NoOfDays |   CostPerDay |
|----+-------------+---------------+-----------------------------+-------------------+-------+------------+--------------|
|  0 | Sunil       |    7869054132 | sunil21@gmail.com           | Srirampura        |    28 |          7 |          500 |
|  1 | Akshay      |    8901234567 | akshay@amphisoft.co.in      | Vijay Nagar       |    27 |          1 |          650 |
|  2 | Krishnanand |    9876543210 | krishnanand@amphisoft.co.in | Ramakrishna Nagar |    28 |          2 |          500 |
+----+-------------+---------------+-----------------------------+-------------------+-------+------------+--------------+

Input: 5
Mahadev,6789098760,mahadev@gmail.com,Srirampura,25,7,500.00
Prasanna,7890345612,prasannaGowda@gmail.com,Vijay Nagar,19,365,1000.00
Sunil,7869054132,sunil21@gmail.com,Srirampura,28,7,500.00
Akshay,8901234567,akshay@amphisoft.co.in,Vijay Nagar,27,1,650.00
Krishnanand,9876543210,krishnanand@amphisoft.co.in,Ramakrishna Nagar,28,2,500.00

Enter the number of bookings
+----+-------------+---------------+-----------------------------+-------------------+-------+------------+--------------+
|    | GuestName   |   PhoneNumber | EmailId                     | Address           |   Age |   NoOfDays |   CostPerDay |
|----+-------------+---------------+-----------------------------+-------------------+-------+------------+--------------|
|  0 | Mahadev     |    6789098760 | mahadev@gmail.com           | Srirampura        |    25 |          7 |          500 |
|  1 | Prasanna    |    7890345612 | prasannaGowda@gmail.com     | Vijay Nagar       |    19 |        365 |         1000 |
|  2 | Sunil       |    7869054132 | sunil21@gmail.com           | Srirampura        |    28 |          7 |          500 |
|  3 | Akshay      |    8901234567 | akshay@amphisoft.co.in      | Vijay Nagar       |    27 |          1 |          650 |
|  4 | Krishnanand |    9876543210 | krishnanand@amphisoft.co.in | Ramakrishna Nagar |    28 |          2 |          500 |
+----+-------------+---------------+-----------------------------+-------------------+-------+------------+--------------+
Solution:
Main.py

```
import pandas as pd

from tabulate import tabulate as tb

df = pd.DataFrame(columns=["GuestName", "PhoneNumber", "EmailId", "Address", "Age", "NoOfDays", "CostPerDay"])

n = int(input("Enter the number of bookings"))

for i in range(n):
    
    data = input().split(",")
    
    if len(data) == 6:
        data.append(None)
        df.loc[i] = data
        
    else:
        df.loc[i] = data
        
f = df['CostPerDay'].astype(float)

df['CostPerDay'] = f.astype(int)

print(tb(df, headers="keys", tablefmt="psql"))
```
