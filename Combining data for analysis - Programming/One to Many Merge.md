# <p align="center">One to Many Merge</p>

Anjali is going to manage the registration data. She is having the data as two dataframes, one is for registration details and another CSV file having the payment details, because currently two persons are handling the data, so the data are in the two separate dataframes. The manager wants to display the data after merging the column nameand bookingDate from registration CSV, and column amountPaid and payment from payment CSV, in one single dataframe as one to many merge for both the files.
So help Anjali to merge both the dataframes.

The following is the 2D format for the registration dataframe:

name,bookingDate,mobNo

The following is the 2D format for the Payment dataframe:

name,amountPaid,finalPayment

Filled the data in the dataframes as the CSV file, in above format.

**Input Format:**
For sample data frame, see the attached zipped file.

**Output Format:**
The output is the dataframe after mering both the dataframes.

Note: Here, the same booking dates for single user, that represents multiple bookings for that user on the same date.

**Sample Input:**
See the attached zipped file, for registration.csv and payment.csv .

**Sample Output:**

```python
name bookingDate  amountPaid  finalPayment
Raju  10-01-2018       12000         18000
Raju  10-01-2018       10000         30000
Amit  10-07-2018        9000         20000
```

**payment.csv**
```python
name,amountPaid,finalPayment
Raju,12000,18000
Amit,9000,20000
Raju, 10000,30000
```

**registration.csv**
```python
name,bookingDate,mobNo
Raju,10-01-2018,9875482575
Amit,10-07-2018,8989898574
```

**Solution:**

```
import pandas as pd

df1 = pd.read_csv("registration.csv")
df2 = pd.read_csv("payment.csv")

df1.columns = ['name', 'bookingDate', 'mobNo']
df2.columns = ['name', 'amountPaid', 'finalPayment']
df1.drop(['mobNo'], axis=1, inplace=True)
print(pd.merge(df1, df2, on=['name']).to_string(index=False))
```

