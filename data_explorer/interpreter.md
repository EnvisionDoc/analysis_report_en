# Interpreter Supported

#### %hive

Example1: Show you how to use hql to query a table raw data.
```sql
%hive
select * from bank limit 10;
```
Click button "run this paragraph", then result is as blow.
![data_explorer_pic](media/data_explorer_pic_3.png)

#### %livy.spark
Example2: Read file "bank.csv" and count the number of rows.
```
%livy.spark
val bank = sc.textFile("/user/data_explore_product_db/spark/input/bank.csv")
bank.count
```
![data_explorer_pic](media/data_explorer_pic_4.png)

#### %livy.pyspark
Example3:
```
```

#### %md
Example4: Supports markdown syntax.
```markdown
%md
# hello world
- **hello world**
```
![data_explorer_pic](media/data_explorer_pic_6.png)


#### %mysql_report
Access the database of BI&Report.  

Example5:
```sql
%mysql_report
select * from bank limit 10;
```
![data_explorer_pic](media/data_explorer_pic_7.png)

Example6:
```sql
%mysql_report
select ${group_by}, count(1)as count, avg(balance)as balance_avg
from bank
where marital="${marital=single,single|divorced|married}" and age < ${maxAge=50}
group by ${group_by=education,education|job|age|marital};
```
![data_explorer_pic](media/data_explorer_pic_8.png)

#### %python
Example7: Show the fundamental operation of python, mark two coordinate points.
```python
%python
import matplotlib.pyplot as plt
z.configure_mpl(width=400, height=300, fmt='svg')
plt.plot([1,2,3,4], [1,4,9,16], 'ro')
```
![data_explorer_pic](media/data_explorer_pic_9.png)

#### %sh
Example8: Show the fundamental operation of shell.
```
%sh
whoami
hadoop fs -ls /user
```
![data_explorer_pic](media/data_explorer_pic_10.png)
