# <p align="center">Many to Many Merge</p>
 
Ankit is working in one of the Insurance company. Ankit is going to manage the credit and debit dataframes. He is having the data as two dataframes, one is for credit details and another CSV file having the debit details, the data are in the two separate dataframes i.e. credit.csv and debit.csv. The manager wants to display the data after merging the column personName, purpose, creditedAmount from credit CSV file, and column debitedAmount from payment CSV file, merge these two in one single dataframe as many to many merge for both the files. Please note that, the merge data frame must show the balance amount from the credited amount.
So help Ankit to merge both the dataframes.

The following is the 2D format for the credit dataframe:

sNo, personName, purpose, creditedAmount

The following is the 2D format for the debit dataframe:

personName, purpose, debitedAmount, date

Filled the data in the dataframes as the CSV file, in above format.

**Input Format:**
For sample data frame, see the attached zipped file.

**Output Format:**
The output is the dataframe after mering both the dataframes.

**Sample Input:**
See the attached zipped file, for credit.csv and debit.csv .

**Sample Output:**
```python
personName    purpose  creditedAmount  debitedAmount  Balance
   Vikram   Marriage           30000          20000    10000
     Amit   Car Loan          400000          50000   350000
   Vikram   Car Loan          500000         100000   400000
   Sachin  Home Loan         1000000         200000   800000
     Amit  Home Loan         2000000         500000  1500000
```

**credit.csv**
```python
sNo,personName,purpose,creditedAmount
1,Vikram,Marriage,30000
2,Amit,Car Loan,400000
3,Vikram,Car Loan,500000
4,Sachin,Home Loan,1000000
5,Amit,Home Loan,2000000
```

**debit.csv**

```python
personName,purpose,debitedAmount,date
Vikram,Marriage,20000,20-11-2018
Amit,Car Loan,50000,22-02-2018
Vikram,Car Loan,100000,30-05-2018
Sachin,Home Loan,200000,10-04-2017
Amit,Home Loan,500000,28-11-2018
```

**Solution:**

```python
import pandas as pd

df1 = pd.read_csv("credit.csv")
df2 = pd.read_csv("debit.csv")

df2.drop(['purpose'], axis=1, inplace=True)

df2['Balance'] = df1['creditedAmount'] - df2['debitedAmount']
df2['Balance'] = df2['Balance'].astype(int)
df2.drop(['personName'], axis=1, inplace=True)
df2.drop(['date'], axis=1, inplace=True)

df1.drop(['sNo'], axis=1, inplace=True)

print(pd.merge(df1, df2,left_index=True, right_index=True,).to_string(index=False))
```
