# Ex-No-4-Creating-Procedures-using-PL-SQL
## AIM:
To create a procedure using PL/SQL.
## STEPS:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table
## PROGRAM:
```
create database emp;
use emp;
drop table employee;
create table employee (empid numeric(10),empname char(10),dept char(15),salary numeric(60));
delimiter //
CREATE PROCEDURE insert_employee_data()
begin
INSERT INTO employee (empid,empname,dept,salary)
VALUES (1,'John','HR',50000);
INSERT INTO employee (empid,empname,dept,salary)
VALUES (2,'Bob','IT',55000);
INSERT INTO employee (empid,empname,dept,salary)
VALUES (3,'joe','Fin',60000);
COMMIT;

END;
//
call insert_employee_data();
select *from employee;
```

## OUTPUT:
![image](https://github.com/AdhithyaMR/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/118834761/78840a50-22dc-4dc4-9c05-6a3f4b0e124c)

## RESULT:
The commands using procedure using PL/SQL has been executed sucessfully.

