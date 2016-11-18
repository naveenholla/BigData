

```python
[cloudera@quickstart ~]$sqoop import-all-tables \
  -m 12 \
  --connect "jdbc:mysql://quickstart.cloudera:3306/retail_db" \
  --username=retail_dba \
  --password=cloudera \
  --as-avrodatafile \
  --warehouse-dir=/user/hive/warehouse/retail_stage.db

hive> create database sqoop_import;
```


```python
#Will see all databases in this warehouse
hive>dfs –ls /user/hive/warehouse;
```
The following data is a Comment, Row formatted fields such as Field terminator, Lines terminator, and Stored File type.

COMMENT ‘Employee details’
FIELDS TERMINATED BY ‘\t’
LINES TERMINATED BY ‘\n

```python
#create Hive database in two different ways: database, schema
hive> CREATE DATABASE userdb;
hive> CREATE SCHEMA userdb;
hive> show databases;
```
OK
default
employee
sqoop_import
user
userdb
Time taken: 0.109 seconds, Fetched: 5 row(s)

```python

```