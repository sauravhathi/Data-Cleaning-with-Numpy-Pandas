# <p align="center">Concatenate the Data using Globbing</p>

Rashmi is going to manage the registration data. He is having the data as multiple dataframes, because currently multiple persons are handling the registration data, so the data are in the multiple separate dataframes. The manager wants to display the data in one single dataframe for multiple dataFrame files.
So help Rashmi to merge all the dataframes.

Def: Glob module finds all the pathnames matching a specified pattern.

The following is the 2D format for the dataframe:
regID, name, date, gender
Filled the data in the dataframe as the CSV file, in above format.

Note: Assume that the data frame name starts as "dataFrame", so the glob will be like glob.glob("dataFrame*.csv") .

**Input Format:**
For sample data frame, see the attached zipped file.

**Output Format:**
The output is the dataframe after mering all the dataframes.

**Sample Input:**
See the attached zipped file, for dataFrame1, dataFrame2, and dataFrame3.

**Sample Output:**

```
regID    name month gender
  101  Vikram   Jan      M
  102    Sasi   Feb      F
  103  Sachin   Apr      M
  104    Amit   Aug      M
  105  Sachin   Apr      M
  106    Amit   Feb      F
```

**dataFrame1.csv**
```python
regID,name,month,gender
101,Vikram,Jan,M
102,Sasi,Feb,F
```

**dataFrame2.csv**
```python
regID,name,month,gender
103,Sachin,Apr,M
104,Amit,Aug,M
```

**dataFrame3.csv**
```python
regID,name,month,gender
103,Sachin,Apr,M
104,Amit,Feb,F
```

**Solution:**

```python
import pandas as pd

df1 = pd.read_csv("dataFrame1.csv")
df2 = pd.read_csv("dataFrame2.csv")
df3 = pd.read_csv("dataFrame3.csv")

print(pd.concat([df1, df2, df3], ignore_index=False).to_string(index=False))
```

