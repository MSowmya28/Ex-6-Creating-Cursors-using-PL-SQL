# Ex. No: 6
## Creating Cursors using PL/SQL

## AIM:
To create a cursor using PL/SQL.

## Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a cursor named as employee_cursor
3. Using cursor read each record and display the result
4. Close the cursor

## Program:
### CREATE A TABLE FOR EMPLOYEE:
```
CREATE TABLE kira (emp_id number,emp_name char(20),emp_dept char(20),emp_salary number);
```
### ISERTING THE VALUES:
```
INSERT INTO kira VALUES (1, 'praneetha', 'Sales', 50000);
INSERT INTO kira VALUES (1, 'nikitha', 'marketing', 60000);
INSERT INTO kira VALUES (3, 'harshini', 'Manager', 70000);
```
### DECLARE CURSOR:
```
DECLARE
CURSOR kira_cursor IS
SELECT emp_id,emp_name,emp_dept,emp_salary
FROM kira;
emp_id NUMBER;
emp_name CHAR(50);
emp_dept CHAR(50);
emp_salary NUMBER;
BEGIN
OPEN kira_cursor;
```
### FETCH AND DISPLAY THE RECORD:
```
LOOP
FETCH kira_cursor INTO emp_id, emp_name, emp_dept, emp_salary;
EXIT WHEN kira_cursor%NOTFOUND;
```
### DISPLAY THE RESULT FOR EACH EMPLOYEE:
```
DBMS_OUTPUT.PUT_LINE('Employee ID: ' || emp_id);
DBMS_OUTPUT.PUT_LINE('Employee Name: ' || emp_name);
DBMS_OUTPUT.PUT_LINE('Department: ' || emp_dept);
DBMS_OUTPUT.PUT_LINE('Salary: ' || emp_salary);
END LOOP;
```
### CLOSE THE CURSOR:
```
CLOSE kira_cursor;
END;
/
```
## Output:
### CREATE A TABLE FOR EMPLOYEE:
![image](https://github.com/dineshgl/Ex-6-Creating-Cursors-using-PL-SQL/assets/94154791/9288e6cf-4c50-4350-a1f4-79b46fe7bd21)



### ISERTING THE VALUES:
![image](https://github.com/dineshgl/Ex-6-Creating-Cursors-using-PL-SQL/assets/94154791/e851f46d-c401-4775-9840-d18b9c506ace)

![image](https://github.com/dineshgl/Ex-6-Creating-Cursors-using-PL-SQL/assets/94154791/5442731e-19b6-4592-bf30-5bc08fd8e614)

### DECLARE CURSOR:
![image](https://github.com/dineshgl/Ex-6-Creating-Cursors-using-PL-SQL/assets/94154791/7eeaec28-775d-433d-aec3-a94d9e6a5785)



### DISPLAY THE RESULT FOR EACH EMPLOYEE:

![image](https://github.com/dineshgl/Ex-6-Creating-Cursors-using-PL-SQL/assets/94154791/1b50b4b0-eec9-445f-9db9-c178bc4636c9)


### Result:
Creating a cursor using SQL/PL has been executed successfully..
