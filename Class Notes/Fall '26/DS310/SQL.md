## Clauses
### SELECT/FROM
```sql
--Specifies which columns should be included
SELECT attribute

--An asterisk means all columns
SELECT *

--Specifies which rows should be included in the result
FROM table_name
```
#### DISTINCT
```sql
--eliminates duplicates
SELECT DISTINCT attributes

--Note: must always be succeeded by a specific attribute
```

### WHERE
```sql
--Dictates a condition of whether a row is included or not
WHERE condition

WHERE condition_1
	AND condition_2 --additional condition that must be fulfilled
	...
```
#### LIKE
```sql
WHERE (attribute LIKE pattern) --used for pattern matching within conditions
--the parenthetical is the condition itself
```
- `%`: 0 or more arbitrary characters
- `_`: A single arbitrary character

### GROUP BY
```sql
--collapses rows that have common values (for aggregate functions)
GROUP BY attribute

--note: WHERE is always applied before the GROUP BY clause
```
### HAVING
```sql
--functions as a conditional filter for grouped items
HAVING condition

--note: HAVING is always applied after the GROUP BY clause
```
### ORDER BY
```sql
--sorts the order by which a query is shown (default ascending from the top down)
ORDER BY attribute 

--note: add DESC to the end to change the order), and a second attribute may be listed to break ties
ORDER BY attribute DESC attribute_2
```
### OUTER JOINS
```sql
FROM table_1 LEFT OUTER JOIN table_2 ON join condition

--can also use RIGHT OUTER JOIN and FULL OUTER JOIN
```
### Comparing NULL (IS/IS NOT)
```sql
--Only way to check for NULL values is to use the IS/NOT IS
...
WHERE attribute IS NULL
...

WHERE attribute IS NOT NULL
```
## Aggregate Functions
*(Note: Cannot be combined with an independent attribute)*
### COUNT()
```sql
--Counts the number of non-null values of an attribute, creating a new column with a row per attribute
SELECT COUNT(attribute)

--Note: like select, can replace attribute with an asterisk, but also counts null values
```
### AVG()
```sql
--finds the average value of an attribute
SELECT AVG(attribute)
```

### MIN/MAX
```sql
--calculates minimum/maximum value found in the attributes
SELECT MIN(attribute)

SELECT MAX(attribute)
```

## Subqueries
```sql
SELECT attribute
FROM table_name
WHERE (subquery
	...
	)

--can also appear in FROM causes
...
FROM (subquery
	...
	... AS name) --some systems require assignment to the subquery
```

### IN/NOT IN
```sql
--used to test for membership within the set (attributes)
...
WHERE attribute NOT IN (
	...)
```
### ALL
```sql
--true when a subquery's attribute value is greater/less than all of the rows in the attribute
...
WHERE attribute > ALL (subquery
	...
	)

--note: attribute = ANY ... is the same as using attribute IN ...
```

### SOME
```sql
--true when a subquery's attribute value is greater/less than at least one of the rows in the attribute
```
## Tables
### CREATE TABLE
```sql
--creates a table with the specified schema
CREATE TABLE table_name (
	column_name_1 datatype_1 constraints_1,
	column_name_2 datatype_2,
...
);
```
### Constraints
#### primary key
```sql
CREATE TABLE table_name (
	... ... PRIMARY KEY --for single-attribute keys
	...
	PRIMARY KEY (column_name_1, column_name_2, ...) --as a composite key
);
```
#### unique
```sql
CREATE TABLE table_name(
	... ... unique, --as a single attribute; specify a non-primary key
	unique(column_name_1, column_name_2,...) --as a composite attribute
);
```

#### not null
```sql
CREATE TABLE table_name(
	... ... not null, --specifies that an attribute canno,
)
```
#### foreign key
```sql
CREATE TABLE table_name (
... ... FOREIGN KEY references external_table, --specifies a foreign key
);
```
### DROP TABLE
```sql
DROP TABLE table_name --deletes an entire table from a database

--note: not possible if there is a foreign-key restraint
```
### INSERT/INTO/VALUES
```sql
INSERT INTO table_name VALUES (attribute_1, attribute_2, ...)
--adds an entry into the table with the provided values (order-sensitive)

INSERT INTO table_name(column_name_1, column_name_2, ...) VALUES attribute_1, attribute_2, ...)
--alternate syntax; allowing for unspecified values to get default values
```
### DELETE
```sql
DELETE FROM table_name --removes specific rows from a table
WHERE condition --specifies what rows get deleted

--note: requires removal of foreign keys attached to removed rows
```

### UPDATE
```sql
UPDATE table_name
SET specified_rows
WHERE condition --specifies which row(s) get modified
``` 
## Data Types
```sql
INTEGER
CHAR(n) --fixed length of n, 
VARCHAR(n) --variable length of up to n
REAL
NUMERIC(n, d) --numeric value up to n, having exactly d digits after its decimal
DATE --format: yyyy-mm-dd
TIME --format: hh:mm:ss
```
### Delimiting Fields
```sql
DATA_TYPE(n)
```
##