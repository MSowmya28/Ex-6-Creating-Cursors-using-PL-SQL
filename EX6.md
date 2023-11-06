# Ex. No: 5 Creating Cursors using PL/SQL

### AIM: To create a cursor using PL/SQL.

### Steps:
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
## OUTPUT
### CREATE A TABLE FOR EMPLOYEE:

![image](https://github.com/MSowmya28/Ex-6-Creating-Cursors-using-PL-SQL/assets/94154791/cc544a55-c86d-4b58-bc53-f66682f25514)


### ISERTING THE VALUES:

![image](https://github.com/MSowmya28/Ex-6-Creating-Cursors-using-PL-SQL/assets/94154791/781bb0b0-7006-4803-b880-c17f4e32cdd2)

![image](https://github.com/MSowmya28/Ex-6-Creating-Cursors-using-PL-SQL/assets/94154791/8779efb1-08d8-41d7-a014-65c75cca0adf)

### DECLARE CURSOR:

![image](https://github.com/MSowmya28/Ex-6-Creating-Cursors-using-PL-SQL/assets/94154791/14fe2b9c-617f-4b16-8fe1-8d36203b0127)

### DISPLAY THE RESULT FOR EACH EMPLOYEE:

![image](https://github.com/MSowmya28/Ex-6-Creating-Cursors-using-PL-SQL/assets/94154791/992164bd-1b15-4b35-a1e8-4b56a9ba57d8)


## RESULT:
Creating a cursor using SQL/PL has been executed successfully..
