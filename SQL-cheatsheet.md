# PostgreSQL Cheatsheet

Each student will complete the Description and Example sections for the SQL clause assigned to them.

For each clause:

1. In the **Description**, explain what the clause does in plain language.main
2. In the **Example**, write a working SQL statement that shows how the clause is used (like the `SELECT and `CREATE TABLE` examples below).
3. As a reference, `SELECT` and `CREATE TABLE` are already done for you.

---

### 1. `SELECT`
   
**Description:** `SELECT *` returns all columns from the provided table. You can also do `SELECT column_name_1, column_name_2` to return specific columns from the provided table.

**Example:**

```sql
SELECT *
FROM movies;
```

### 2. `CREATE TABLE`

**Description:** `CREATE TABLE` creates a new table in a database. It allows one to specify the name of the table, the name of each column, and each column's data type in the table.

**Example:**

```sql
CREATE TABLE friends (
  friend_id SERIAL PRIMARY KEY,
  name VARCHAR,
  birthday DATE
);
```

### 3. `INSERT INTO` — assigned to Ainslie

**Description:** 

**Example:**

```sql

```

### 4. `UPDATE` — assigned to Babz

**Description:** 

**Example:**

```sql

```

### 5. `DELETE FROM` — assigned to Haine

**Description:** 

**Example:**

```sql

```

### 6. `GROUP BY` — assigned to Jackie

**Description:** 

**Example:**

```sql

```

### 7. `ORDER BY` — assigned to Jenny

**Description:** 

**Example:**

```sql

```

### 8. `INNER JOIN` — assigned to Megan

**Description:** 

**Example:**

```sql

```

### 9. `LIMIT` — assigned to Mimi

**Description:** 

**Example:**

```sql

```

### 10. `ON CONFLICT` — assigned to Priscilla

**Description:** `ON CONFLICT` checks for duplicate values. After a conflict is found, if you gave your query instructions as to how to handle the conflict, it will do so.

**Example:**
Lets say that you create a table of countries and `INSERT` the following.
```sql
INSERT INTO country_counts (country_name, count)
VALUES	('Mexico', 1),
		('Cuba', 1),
        ('Brazil', 1),
        ('Ethiopia', 1);
```
This creates a table with both a country and an assigned value into the `count` column. The data type of which, is `INTEGER`.
Then, lets say that you attempt to `INSERT` 'mexico' again.

```sql
INSERT INTO country_counts (country_name, count)
VALUES ('Mexico', 1)
ON CONFLICT (country_name)
DO UPDATE SET count = country_counts.count + 1
RETURNING count;
```
Instead of crashing and returning an error, our `INSERT` will instead see the conflict. In this case, specifically a conflict in our `country_name`. The following line gives the query instructions to follow. In this query, we take the count value and add 1 to the `INTEGER`. Following that, we have the query return the value of `count`.


### 11. `LIKE` — assigned to Stephanie

**Description:** 

**Example:**

```sql

```

### 12. `COUNT` — assigned to Tee

**Description:** 

**Example:**

```sql

```
