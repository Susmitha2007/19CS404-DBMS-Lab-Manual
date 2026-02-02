# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**

<img width="732" height="315" alt="Screenshot 2026-02-02 133304" src="https://github.com/user-attachments/assets/c7f11a5f-1837-4cdd-8884-c0198f2bffc5" />

**Output:**

<img width="1316" height="678" alt="Screenshot 2026-02-02 133406" src="https://github.com/user-attachments/assets/18525f28-19b2-4c1b-b822-55506786acd1" />

**Question 2**

<img width="799" height="406" alt="Screenshot 2026-02-02 133812" src="https://github.com/user-attachments/assets/5ce3fcf0-73f5-4bb4-8304-ee65d45f5195" />

**Output:**

<img width="1215" height="683" alt="Screenshot 2026-02-02 133829" src="https://github.com/user-attachments/assets/cc6d73a1-84ab-4b58-80ab-9685dcada50c" />

**Question 3**

<img width="827" height="180" alt="Screenshot 2026-02-02 133918" src="https://github.com/user-attachments/assets/9165e762-ea59-4abf-b153-2f23c541c0bf" />

**Output:**

<img width="1219" height="607" alt="Screenshot 2026-02-02 133932" src="https://github.com/user-attachments/assets/a7fa6bfe-7d44-41cc-bb63-c4fd8159ecbd" />

**Question 4**

<img width="1010" height="232" alt="Screenshot 2026-02-02 134147" src="https://github.com/user-attachments/assets/ac02a316-79b0-48ab-94b6-e2143d3c7a1b" />

**Output:**

<img width="1325" height="621" alt="Screenshot 2026-02-02 134205" src="https://github.com/user-attachments/assets/36a8108a-5949-4fd9-a889-6c8f0c54b964" />

**Question 5**

<img width="634" height="340" alt="Screenshot 2026-02-02 134247" src="https://github.com/user-attachments/assets/70e21822-005c-4568-b418-d3ebc50abe62" />

**Output:**

<img width="1120" height="647" alt="Screenshot 2026-02-02 134309" src="https://github.com/user-attachments/assets/bf54f179-b4a4-4a56-8ccc-2e5e01fb9a45" />

**Question 6**

<img width="1322" height="182" alt="Screenshot 2026-02-02 134354" src="https://github.com/user-attachments/assets/e3f08056-9f4e-46ca-b471-8f4c2b805e2f" />

**Output:**

<img width="1311" height="680" alt="Screenshot 2026-02-02 134407" src="https://github.com/user-attachments/assets/189e9f0e-d5b4-4345-9e6d-52667b115ca3" />

**Question 7**

<img width="722" height="239" alt="Screenshot 2026-02-02 134453" src="https://github.com/user-attachments/assets/266ab853-b311-42e4-8cde-0c582416c531" />

**Output:**

<img width="1242" height="688" alt="Screenshot 2026-02-02 134506" src="https://github.com/user-attachments/assets/102dbe93-418f-4092-8e5d-a2890d4c6510" />

**Question 8**

<img width="1071" height="315" alt="Screenshot 2026-02-02 134552" src="https://github.com/user-attachments/assets/c240389c-af12-435f-9180-69e7f02ce1e6" />

**Output:**

<img width="1302" height="669" alt="Screenshot 2026-02-02 134613" src="https://github.com/user-attachments/assets/d677ccec-3570-4636-bb35-083a4ae7358e" />

**Question 9**

<img width="564" height="257" alt="Screenshot 2026-02-02 134704" src="https://github.com/user-attachments/assets/0b7c7800-35cc-4db0-bda1-f97ba03d1388" />

**Output:**

<img width="1260" height="673" alt="Screenshot 2026-02-02 134722" src="https://github.com/user-attachments/assets/c0ed4d93-5ed2-458e-9baa-a1585e0a7950" />

**Question 10**

<img width="656" height="272" alt="Screenshot 2026-02-02 134839" src="https://github.com/user-attachments/assets/52729972-07dc-48c3-8de6-6101d8dfa6d6" />

**Output:**

<img width="1246" height="693" alt="Screenshot 2026-02-02 134818" src="https://github.com/user-attachments/assets/3c6bbf76-3ac9-4aff-a12e-15b02d36e7ae" />

## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
