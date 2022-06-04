# <p align="center">Column Wise Merging</p>

Abhishek is going to manage the registration data. He is having the data as two dataframes, because currently two persons are handling the registration data, so the data are in the two separate dataframes. The manager wants to display the data in one single dataframe, but merge as column wise.
So help Abhishek to merge both the dataframes.

The following is the 2D format for the dataframe:   
regID, name, date, gender
Filled the data in the 2 dataframe as the CSV files named as dataFrame1 and dataFrame2, in above format.

**Input Format:**
For sample data frame, see the attached zipped file.

**Output Format:**
The output is the dataframe after mering both the dataframes as column wise.

**Sample Input:**
See the attached zipped file, for dataFrame1 and dataFrame2.

**Sample Output: **
```python
regID    name        date gender
  101  Vikram  10-02-2019      M
  102    Sasi  15-04-2020      F
  103  Sachin  12-09-2015      M
  104    Amit  20-02-2013      F
  ```
  
**dataFrame1.csv**
```python 
egID,name,date,gender
101,Vikram,10-02-2019,M
102,Sasi,15-04-2020,F
```
**dataFrame2.csv**
```python 
regID,name,date,gender
103,Sachin,12-09-2015,M
104,Amit,20-02-2013,F
```

**Solution:**

```python
import pandas as pd

dataFrame1 = pd.read_csv("dataFrame1.csv")
dataFrame2 = pd.read_csv("dataFrame2.csv")
print(pd.merge(dataFrame1, dataFrame2, how='outer').to_string(index=False))
```

Happy Coding
