# Product - > Item

"Lakshmi Stationaries" famous and wholesale stationary shop in Hyderabad, the shop was built by Lakshmi Prasad's father Suresh Prasad. During his time in order to store the count or work on the item in the shop, they used the dataset columns name as "ProductId", "ProductName", "ProductCount" etc... But Lakshmi Prasad felt that columns should be named as ItemId, ItemName, ItemCount etc.. but wanted to retain all other data in the dataset.

**Input-Output Format:**
Input will be provided through a CSV file say it top be(product.csv).

**Sample Input-Output:**
**product.csv**

``sql
DataSet when SureshPrasad is handling

+---+-----------+-------------+--------------+--------------+
|   | ProductId | ProductName | ProductPrice | ProductCount |
+---+-----------+-------------+--------------+--------------+
| 0 |    100    |     Pen     |      10      |     100      |
| 1 |    101    |    Sheet    |      1       |     1000     |
| 2 |    102    |     Book    |      25      |      30      |
| 3 |    103    |    Pencil   |      3       |     200      |
| 4 |    104    |     Ink     |      35      |      10      |
| 5 |    105    |     Box     |      45      |      5       |
+---+-----------+-------------+--------------+--------------+
DataSet when LakshmiPrasad is handling
+---+--------+----------+-----------+-----------+
|   | ItemId | ItemName | ItemPrice | ItemCount |
+---+--------+----------+-----------+-----------+
| 0 |  100   |   Pen    |     10    |    100    |
| 1 |  101   |  Sheet   |     1     |    1000   |
| 2 |  102   |   Book   |     25    |     30    |
| 3 |  103   |  Pencil  |     3     |    200    |
| 4 |  104   |   Ink    |     35    |     10    |
| 5 |  105   |   Box    |     45    |     5     |
+---+--------+----------+-----------+-----------+
``


Happy Coding