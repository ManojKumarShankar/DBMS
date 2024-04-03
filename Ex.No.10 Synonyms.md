# EXP NO 10: SYNONYMS AND ASSERTIONS IN SQL 
### DATE: 18/10/23

## AIM:
To create a student database and create a synonym and assertions.

## THEORY
## SYNONYM
<div align="justify">
A SYNONYM provides another name for database object, referred to as original object, that may exist on a local or another server.
</div>
## ASSERTIONS
<div align="justify">
* An assertion is a piece of SQL which makes sure a condition is satisfied, else or it stops the action being taken on a database.
* An assertion is a constraint that might be dependent upon multiple rows of multiple tables.
</div>

## Query:
### 1) Create a table EMPLOYEE and perform insertion of two rows.

### SQL QUERY: 
```
CREATE TABLE EMPLOYEE (
    employee_id INT ,
    name VARCHAR(255),
    department VARCHAR(255),
    salary DECIMAL(10, 2)
);
```


### OUTPUT:
![image](https://github.com/ManojKumarShankar/DBMS/assets/122000959/cde7cb9f-6c7c-4913-aaf1-fd8ca37346c9)
![image](https://github.com/ManojKumarShankar/DBMS/assets/122000959/75f55cbb-92b9-463c-8039-687b4a1e008f)






### 2) Create a synonym S1 for EMPLOYEE  table.

### SQL QUERY: 
```
CREATE SYNONYM S1 FOR EMPLOYEE;
```

### OUTPUT:
![image](https://github.com/ManojKumarShankar/DBMS/assets/122000959/cdad73ba-e485-46fd-8e3b-296df67c26d6)





### 3) Display the EMPLOYEE  table using synonym S1.
 
### SQL QUERY: 
```
SELECT * FROM S1;
```


### OUTPUT:
![image](https://github.com/ManojKumarShankar/DBMS/assets/122000959/72058de7-2e91-4bf8-b814-29bcdbab2720)




### 4) Drop the synonym.

### SQL QUERY: 
```
DROP SYNONYM S1;
```


### OUTPUT:
![image](https://github.com/ManojKumarShankar/DBMS/assets/122000959/2ac2be05-f6b4-4d78-a532-fd96733a05fa)



### 5) Create a supplier table and create a sequence S2 for supplier table id.

### SQL QUERY: 
```
CREATE TABLE supplier (
    id INT,
    name VARCHAR(255),
    address VARCHAR(255),
    contact_person VARCHAR(255)
);

CREATE SEQUENCE S2 START 1;

```


### OUTPUT:
![image](https://github.com/ManojKumarShankar/DBMS/assets/122000959/5675815a-0ffb-45f6-86d4-ab94267998a2)

![image](https://github.com/ManojKumarShankar/DBMS/assets/122000959/5aa899a5-f354-4fd4-97c1-56ac65928535)



### 6) insert the data into supplier table use sequence.

### SQL QUERY: 
```
INSERT INTO supplier (id, name, address, contact_person)
VALUES (NEXTVAL('S2'), 'ABC Suppliers', '123 Main Street', 'John Doe');

INSERT INTO supplier (id, name, address, contact_person)
VALUES (NEXTVAL('S2'), 'XYZ Distributors', '456 Elm Road', 'Jane Smith');
```


### OUTPUT:
![image](https://github.com/ManojKumarShankar/DBMS/assets/122000959/06b0364d-5f56-48be-b8b4-4e09da616b44)



### 7) Drop the sequence

### SQL QUERY: 
```
DROP SEQUENCE S2;
```

### OUTPUT:
![image](https://github.com/ManojKumarShankar/DBMS/assets/122000959/a7a18351-c449-43ec-8dd9-0c7c99925b14)



## RESULT :
Thus the sequence and synonym created and used in SQL.
