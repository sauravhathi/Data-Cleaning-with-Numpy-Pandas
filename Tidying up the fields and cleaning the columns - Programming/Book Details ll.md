Book Details ll
 
The Government decided to open a central library with respect ever area finding a librarian in the rural area was a difficult task so they wanted to build an automated system which does the work of a librarian making note of the book details taken by the public for their reference. 
When it comes to collecting the data required data was bookName, PublishedDate, PublishedBy, PlaceOfPublication.  The common thing observed was public used to entire some wrong details wrt place of publication, In order to avoid such error, they prefixed PlaceofPublication wrt some state name[like Karnataka, New Delhi].

So Write a program in such a way that it should accept the placeofpublication with the state name only if it consists [Karnataka, New Delhi] in the entire data else should be replaced with NaN .

Input-output Format:
The first line of the input consists of an integer corresponding to the number of books taken by the public.
The Next n line consists of book details as CSV(comma separated values) with corresponding details like {  BookName, PublishingYear, PublishedBy, PlaceOfPublication }

Please refer sample input-output for better understanding.

**Sample Input-Output:**
```python
Enter the number of books
3
El Dorado,1973,Ananth,Kolar Gold Field Karnataka
Thugs Of Malgudi,1890,Rakshith, Mangalore Karnataka
2 State,2010,Chethan Bhagat ,New Delhi
+---+------------------+----------------+-----------------+--------------------+
|   |     BookName     | PublishingYear |   PublishedBy   | PlaceOfPublication |
+---+------------------+----------------+-----------------+--------------------+
| 0 |    El Dorado     |      1973      |      Ananth     |     Karnataka      |
| 1 | Thugs Of Malgudi |      1890      |     Rakshith    |     Karnataka      |
| 2 |     2 State      |      2010      | Chethan Bhagat  |     New Delhi      |
+---+------------------+----------------+-----------------+--------------------+
```

**Additional Sample TestCases
Sample Input and Output 1 :**

```python
Enter the number of books
3
El Dorado,1973,Ananth,Kolar Gold Field Karnataka
Thugs Of Malgudi,1890,Rakshith, Mangalore Karnataka
2 State,2010,Chethan Bhagat ,New Delhi
+---+------------------+----------------+-----------------+--------------------+
|   |     BookName     | PublishingYear |   PublishedBy   | PlaceOfPublication |
+---+------------------+----------------+-----------------+--------------------+
| 0 |    El Dorado     |      1973      |      Ananth     |     Karnataka      |
| 1 | Thugs Of Malgudi |      1890      |     Rakshith    |     Karnataka      |
| 2 |     2 State      |      2010      | Chethan Bhagat  |     New Delhi      |
+---+------------------+----------------+-----------------+--------------------+
```

**Sample Input and Output 2 :**

```python
Enter the number of books
2
Vada Chennai,2008,Danush,Chennai
Girl next door,2013,Chetha Bhagat,Shalimarbagh New Delhi
+---+----------------+----------------+---------------+--------------------+
|   |    BookName    | PublishingYear |  PublishedBy  | PlaceOfPublication |
+---+----------------+----------------+---------------+--------------------+
| 0 |  Vada Chennai  |      2008      |     Danush    |        nan         |
| 1 | Girl next door |      2013      | Chetha Bhagat |     New Delhi      |
+---+----------------+----------------+---------------+--------------------+
```

**Solution:**

```python
import pandas as pd
from tabulate import tabulate

print("Enter the number of books")
n = int(input())
df = pd.DataFrame(columns=['BookName', 'PublishingYear', 'PublishedBy', 'PlaceOfPublication'])
for i in range(n):
    arr = input().split(",")
    df.loc[i] = arr

if df['PlaceOfPublication'].str.contains('Karnataka').any():
    df['PlaceOfPublication'] = df['PlaceOfPublication'].str.extract('(Karnataka)', expand=True)
else:
    df['PlaceOfPublication'] = "nan"

print(tabulate(df[[ 'BookName', 'PublishingYear', 'PublishedBy', 'PlaceOfPublication']], headers='keys', tablefmt='psql'))
```
