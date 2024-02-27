---
aliases:
  - SQL Joins
---
# Postgres joins
The same input with be used to demonstrate these joins:
**Input:**
```
 a | fruit_a
---+----------
 1 | Apple
 2 | Orange
 3 | Banana
 4 | Cucumber
(4 rows)
 b |  fruit_b
---+------------
 1 | Orange
 2 | Apple
 3 | Watermelon
 4 | Pear
(4 rows)
```
First table is table $\textcolor{red}{A}$
Second table is table $\textcolor{aqua}{B}$
## Inner join
1. The inner join examines each row in table $\textcolor{red}{A}$.
2. For each row it compares the value in the $\textcolor{red}{A}$'s column with the value in the $\textcolor{aqua}{B}$'s column. 
3. If these values are equal, the inner join adds to the result a new row that contains columns from both tables.
![[Pasted image 20240226210630.png]]
### Example
**Query:**
```sql
SELECT * FROM basket_a
INNER JOIN basket_b
    ON fruit_a = fruit_b;
```
**Output**
```
 a | fruit_a | b | fruit_b
---+---------+---+---------
 1 | Apple   | 2 | Apple
 2 | Orange  | 1 | Orange
(2 rows)
``` 
## Left outer join
![[Pasted image 20240226210910.png]]
1. The left join examines each row in table $\textcolor{red}{A}$.
2. For each row it compares the value in the $\textcolor{red}{A}$'s column with the value in the $\textcolor{aqua}{B}$'s column. 
3. If these values are equal, the left join adds to the result a new row that contains columns from both tables.
4. If the values are not equal, the left join also adds to the result a new row that contains columns from both tables. Missing values are replaced with null.
### Example
**Query:**
```sql
SELECT * FROM basket_a
LEFT JOIN basket_b
	ON fruit_a = fruit_b;
```
**Output**
```
 a | fruit_a  |  b   | fruit_b
---+----------+------+---------
 3 | Banana   | null | null
 4 | Cucumber | null | null
(2 rows)
```

## Right outer join
![[Pasted image 20240226210921.png]]
1. The right join examines each row in table $\textcolor{aqua}{B}$.
2. For each row it compares the value in the $\textcolor{aqua}{B}$'s column with the value in the $\textcolor{red}{A}$'s column. 
3. If these values are equal, the right join adds to the result a new row that contains columns from both tables.
4. If the values are not equal, the right join also adds to the result a new row that contains columns from both tables. Missing values are replaced with null.
### Example
**Query:**
```sql
SELECT * FROM basket_a
RIGHT JOIN basket_b
	ON fruit_a = fruit_b;
```
**Output**
```
  a   | fruit_a | b |  fruit_b
------+---------+---+------------
 null | null    | 3 | Watermelon
 null | null    | 4 | Pear
(2 rows)
```
## Full outer join
![[Pasted image 20240226210900.png]]
1. The inner join examines each row in table $\textcolor{red}{A}$ and $\textcolor{aqua}{B}$.
2. For each row it compares the value in the $\textcolor{red}{A}$'s column with the value in the $\textcolor{aqua}{B}$'s column. 
3. If these values are equal, the full join adds to the result a new row that contains columns from both tables.
4. If the values are not equal, the full join also adds to the result a new row that contains columns from both tables. Missing values are replaced with null.
### Example
**Query:**
```sql
SELECT * FROM basket_a
FULL JOIN basket_b
	ON fruit_a = fruit_b;
```
**Output**
```
  a   | fruit_a  |  b   |  fruit_b
------+----------+------+------------
    1 | Apple    |    2 | Apple
    2 | Orange   |    1 | Orange
    3 | Banana   | null | null
    4 | Cucumber | null | null
 null | null     |    3 | Watermelon
 null | null     |    4 | Pear
(6 rows)
```
## Joins cheat sheet
![[Pasted image 20240226213729.png]]
# DBMS Joins
The same input with be used to demonstrate these joins:
**Input:**
```
 column 1 | column 2
----------+----------
 1        | 1
 1        | 2
(2 rows)
  column 1 | column 2
----------+----------
 1        | 1
 1        | 3
(2 rows)
```
## Theta join
A subdivision of the [[#Inner join]]. Basically, a join that occurs according to condition $\theta$.
$$
A \bowtie_{\theta} B
$$
### Example
**Query:**
$$
A \bowtie_{A.column\ 2 > B.column\ 2} B
$$
**Output:**
```
 column 1 | column 2
----------+----------
 1        | 2
(1 row)
```
## EQUI Join
A subdivision of the [[#Inner join]]. [[#Theta join]], if the $\theta$ condition is the equality condition.
### Example
**Query:**
$$
A \bowtie_{A.column\ 2\ =\ B.column\ 2} B
$$
```
 column 1 | column 2
----------+----------
 1        | 1
(1 row)
```
## Natural Join
A subdivision of the [[#Inner join]]. In this type of join, the attributes should have the same name and domain. It performs selection forming equality on those attributes, which appear in both relations and eliminates the duplicate attributes.
$$
C \bowtie D
$$
# References
- https://www.postgresqltutorial.com/postgresql-tutorial/postgresql-natural-join/
- https://www.guru99.com/joins-sql-left-right.html#types-of-join