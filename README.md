# EX-3-SubQueries-Views-and-Joins
# Create employee Table

CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));

# Insert the values

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7369, 'SMITH', 'CLERK', 7902, '17-DEC-80', 800, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-81', 1600, 300, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7521, 'WARD', 'SALESMAN', 7698, '22-FEB-81', 1250, 500, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7566, 'JONES', 'MANAGER', 7839, '02-APR-81', 2975, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-81', 1250, 1400, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7698, 'BLAKE', 'MANAGER', 7839, '01-MAY-81', 2850, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7782, 'CLARK', 'MANAGER', 7839, '09-JUN-81', 2450, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7788, 'SCOTT', 'ANALYST', 7566, '19-APR-87', 3000, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7839, 'KING', 'PRESIDENT', NULL, '17-NOV-81', 5000, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7844, 'TURNER', 'SALESMAN', 7698, '08-SEP-81', 1500, 0, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7876, 'ADAMS', 'CLERK', 7788, '23-MAY-87', 1100, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7900, 'JAMES', 'CLERK', 7698, '03-DEC-81', 950, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('03-DEC-81', 'DD-MON-RR'), 3000, 20, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('23-JAN-82', 'DD-MON-RR'), 1300, 10, 10);

# Create department table

CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));

# Insert the values in the department table

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');

# Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.

# QUERY:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/175818d7-da7e-4987-b7e9-cfde64f45f72)

OUTPUT:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/f053a3cb-0970-46de-a16d-a76303dcdf0f)

# Q2) List the ename,job,sal of the employee who get minimum salary in the company.

# QUERY:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/dd447eb2-2ebf-47b5-b0a7-6f82613b2dd4)

# OTUPUT:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/89c9ec99-d84a-4a51-ac78-af87eb58983b)

# Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

# QUERY:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/8939827a-8f38-448a-a582-79453f2df4f9)

# OUTPUT:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/97349dda-0313-4c77-b754-e5954fae968a)

# Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

# QUERY:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/64cd660a-4be6-4458-a7d5-48017c9cb8f7)

# OUTPUT:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/34b25b2d-52f9-41d4-8149-9db6792639a4)

# Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

# QUERY:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/5d37fa2c-8b49-4dd5-8337-ffed5ec19dc4)

# OUTPUT:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/3f45bf5a-3b47-467a-b9f8-d5dbe264e6e9)

# Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

# QUERY:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/6b77c191-0ea3-4f50-869a-37672957e545)

# OUTPUT:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/db6fee2f-b596-4f67-9062-8ef396b6469b)

# Create a Customer1 Table

CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);

# Inserting Values to the Table

INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001); INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001); INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002); INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002); INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006); INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003); INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007); INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);

# Create a Salesperson1 table

CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));

# Inserting Values to the Table

INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15); INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13); INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11); INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14); INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13); INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);

# Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

# QUERY:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/0a0523e0-d124-4871-8b70-ec50901fb384)

# OUTPUT:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/1320b2a9-242d-429a-889f-2b82f76ba5d8)

# Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.

# QUERY:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/44f61b24-489b-4d2c-93d5-e0e73af4ec28)

# OUTPUT:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/d3727c0e-2529-4e01-acdb-89153d2b94d5)

# Q9) Perform Natural join on both tables

# QUERY:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/f870c5e7-29a2-4bcc-833c-4da457650ea1)

# OUTPUT:

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/c4c803cb-a614-4499-8371-fe26fc93e189)

# Q10) Perform Left and right join on both tables

# Left Join

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/caa7dbba-a560-4063-a8aa-3f0931596a8a)

# Right Join

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/57b202f5-f975-430f-8970-ee82a7e9911a)

# OUTPUT:

# Left Join

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/33913cae-36c0-4a30-845a-61dcfe976ebb)

# Right Join

![image](https://github.com/POKALAGURAVAIAH8121/EX-3-SubQueries-Views-and-Joins/assets/128034765/1d85da9c-b90d-459a-9fc2-8998af0dc42f)
