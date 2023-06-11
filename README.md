# Exp-4-SQL-query-to-show-record-from-one-table-that-another-table-does-not-have
## AIM:
### To show that the records of one table doesnot exists in another table by using SQL.
## ALGORITHM:
### STEP 1: Create a sample table in SQL using CREATE TABLE syntax
### STEP 2: Insert all the values and Titles respectively using INSERT INTO syntax
### STEP 3: Now check whether all the rows are affected or not by fetching the table
### STEP 4: After checking, now use SELECT for choosing the column name that we want and use FROM to choose the table
### STEP 5: Then use WHERE to check the condition and NOT IN syntax to check whether the column or table mention is there in another table
### STEP 6: After compiling and running the program, the results will be displayed.
## PROGRAM:
```
create table office1(
  Sno int,
  Department varchar(50),
  No_of_workers int,
  avg_salary_pm int
);
insert into office1 (Sno,Department,No_of_workers,avg_salary_pm)
values (1,'Development',15,100000);
insert into office1 (Sno,Department,No_of_workers,avg_salary_pm)
values (2,'Frontend Dv',10,70000);
insert into office1 (Sno,Department,No_of_workers,avg_salary_pm)
values (3,'Backend DV',7,75000);
insert into office1 (Sno,Department,No_of_workers,avg_salary_pm)
values (4,'Finance MM',8,50000);
insert into office1 (Sno,Department,No_of_workers,avg_salary_pm)
values (5,'Designer',12,65000);
insert into office1 (Sno,Department,No_of_workers,avg_salary_pm)
values (6,'Marketing',25,55000);
insert into office1 (Sno,Department,No_of_workers,avg_salary_pm)
values (7,'Chief heads',4,150000);
insert into office1(Sno,Department,No_of_workers,avg_salary_pm)
values (8,'Law persuit',3,45000);

create table office2(
  Sno int,
  Department varchar(50),
  No_of_workers int,
  avg_salary_pm int
);
insert into office2 (Sno,Department,No_of_workers,avg_salary_pm)
values (1,'Cybersecurity',5,100000);
insert into office2 (Sno,Department,No_of_workers,avg_salary_pm)
values (2,'Purchase Dept',9,65000);
insert into office2 (Sno,Department,No_of_workers,avg_salary_pm)
values (3,'Finance MM',7,65000);
insert into office2 (Sno,Department,No_of_workers,avg_salary_pm)
values (4,'Operations MM',6,60000);
insert into office2 (Sno,Department,No_of_workers,avg_salary_pm)
values (5,'General Dept',12,65000);
insert into office2 (Sno,Department,No_of_workers,avg_salary_pm)
values (6,'Marketing dept',25,95000);
insert into office2 (Sno,Department,No_of_workers,avg_salary_pm)
values (7,'Chief heads',5,150000);
insert into office2(Sno,Department,No_of_workers,avg_salary_pm)
values (8,'Law persuit',7,55000);

select *from office1
where Department not in 
  (select Department
  from office2);
  ```

## OUTPUT:
![image](https://github.com/gpavithra673/Exp-4-SQL-query-to-show-record-from-one-table-that-another-table-does-not-have./assets/93427264/6dacdf88-1e4a-45d6-81d9-8dbb581f206d)
## RESULT:
### Thus we have successfully obtained the required result using the above-given code.
