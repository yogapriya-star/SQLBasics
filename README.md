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
    student_id int,
    name varchar(100),
    age int,
    department varchar(100),
    student_mark int
 )   
```

To add a column in existing table
```bash
alter table student add column degree varchar(100)
```

To change the column name in existing table
```bash
alter table student change dept department varchar(100)
```

To rename the column name in existing table
```bash
alter table student rename column department to dept
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
insert into student values(1,"John",25,"CSE",90)
```

To insert multiple row in table
```bash
insert into student values(2,"Praveen",45,"ECE",85),(3,"Suresh",34,"EEE",88);
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

To delete the specific column in table
```bash
alter table student drop column department
```

**DQL Command**

To select the table
```bash
select * from student
```

To select the particular column from table
```bash
select name, dept from student
```

To select the distinct data where the student is from  a department="EEE" from table
```bash
select * from student where department="EEE"
```

To print the data where the student IDs who are greater than 2 from table
```bash
select * from student where student_id>2
```

**Aggregate Function**
SUM()

SUM() of stundent_mark from student table
```bash
select sum(student_mark) from student 
```

SUM() of stundent_mark from student table by giving the alice name for the column
```bash
select sum(student_mark) as total_mark from student 
```

MAX()

MAX() of stundent_mark from student table
```bash
select max(student_mark) as maximum_mark from student 
```

MIN()

MIN() of stundent_mark from student table
```bash
select min(student_mark) as minimum_mark from student 
```

AVG()

AVG() of stundent_mark from student table
```bash
select avg(student_mark) as average_mark from student 
```

COUNT()

COUNT() of stundent_mark from student table where department="EEE"
```bash
select count(student_mark) as student_count_mark from student where department="EEE"
```

**Order By**

order by specific column in to descending order in student table 
```bash
select name,student_mark from student order by student_mark desc
```

order by specific column in to acsending order in student table 
```bash
select name,student_mark from student order by student_mark asc
```

list all students in alphabetical order by name in student table 
```bash
select * from student order by name asc
```

list all students in the EEE department and sort them by mark in descending order in student table 
```bash
select * from student where student_mark<500 order by department desc
```

**Group By**

Select specific column and use group by with aggregate function in student table 
```bash
select avg(student_mark) as average_mark,department from student group by department="EEE"
```

group by specific column add aggregate function in student table 
```bash
select avg(student_mark) as average_mark,department from student group by department
```

find the total number of students in each department in student table 
```bash
select count(*) as department_count, department from student group by department_count
```

**Group By** **Order By**

group by specific column add aggregate function with order by in student table 
```bash
select count(student_mark) as student_count, department from student group by department order by student_count desc
```

calculate the average mark for each department and sorted in ascending order by department name in student table 
```bash
select avg(student_mark) as avg_student_mark, department from student group by department order by department asc
```

find the department with the highest average mark in student table 
```bash
select avg(student_mark) as avg_student_mark, department from student group by department order by avg_student_mark desc limit 1
```

find the department with the lowest average mark in student table 
```bash
select avg(student_mark) as avg_student_mark, department from student group by department order by avg_student_mark asc limit 1
```

**Having Clause**

select the department with the average mark using condition that average mark should be less than 500 in student table 
```bash
select avg(student_mark) as avg_student_mark, department from student group by department having avg_student_mark >500
```

**OR Condition**

select the name either William Turner or  ALice Brown in student table 
```bash
select * from student where name="William Turner" or name="ALice Brown"
```
