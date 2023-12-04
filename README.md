# SQLBasics
Standard Query Language

**DDL Command**

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
create table student(
    name varchar(100),
    age int,
    department varchar(100)
 )   
```

To add a column in existing table
```bash
alter table student add column degree varchar(100)
```

To change the column name in existing table
```bash
alter table student change department dept varchar(100)
```

To change the data type for column in existing table
```bash
alter table student change age age varchar(100)
```

To drop the table
```bash
drop table student
```

To delete all the data from table
```bash
truncate table student
```

**DML Command**

To insert the data in table
```bash
insert into student values("John",25,"CSE")
```

To insert multiple row in table
```bash
insert into student values("Praveen",45,"ECE"),("Suresh",34,"EEE");
```

To update the column in table
```bash
update student set age=23
```

To update the particular column using where condition in table
```bash
update student set age=23 where age=45
```

To update the particular column using where condition in table
```bash
update student set age=22 where name="Praveen"
```

To delete the table
```bash
delete from student
```

To delete the particular column using where condition in table
```bash
delete from student where department="ECE"
```

To delete all the data where the column in null in table
```bash
delete from student where department is null
```

**DQL Command**

To select the table
```bash
select * from student
```
