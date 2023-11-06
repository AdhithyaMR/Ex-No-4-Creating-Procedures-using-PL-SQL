# Ex-No-4-Creating-Procedures-using-PL-SQL
## DATE: 24/08/2023
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
```SQL
SQL> CREATE TABLE es(
     empid NUMBER,
     empname VARCHAR(10),
     dept VARCHAR(10),
     salary NUMBER
    );
CREATE OR REPLACE PROCEDURE emp_data AS
    BEGIN
    INSERT INTO es(empid,empname,dept,salary)
    values(1,'NAGUL','AIDS',100000);
    INSERT INTO es(empid,empname,dept,salary)
    values(2,'VINOD','AIML',100000);
    INSERT INTO es(empid,empname,dept,salary)
    values(3,'ARVIND','AIML',100000);
    COMMIT;
   FOR emp_rec IN (SELECT * FROM es)LOOP
   DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||
   ',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
   END LOOP;
   END;
  /
```

## OUTPUT:
![270942742-d7c0a2aa-eb7a-4abe-84d1-70f8fb28f01e](https://github.com/AdhithyaMR/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/118834761/0d182b4f-e8a4-4161-8fc1-b09e11ce5e82)




## RESULT:
The commands using procedure using PL/SQL has been executed sucessfully.

