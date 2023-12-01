# SQLBasics
Standard Query Language

To create a database in MYSQL Workbench
```bash
create schema dummy
```
To select the dummy database
```bash
use dummy
```

To create a table in dummy database and add data 
```bash
create table teacher(
	name varchar(100),
    age int,
    salary int,
    department varchar(100)
 )   
```

To add a column in existing table
```bash
alter table teacher add column degree varchar(100)
```

To change the column name in existing table
```bash
alter table teacher change department dept varchar(100)
```
