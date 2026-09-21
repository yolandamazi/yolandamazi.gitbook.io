# SQLBolt Lessons

## SQL Lesson 1: SELECT queries 101

### Select query for a specific columns

```sql
SELECT column, another_column, …
FROM mytable;
```

### Select query for all columns

```sql
SELECT * 
FROM mytable;
```

## SQL Lesson 2: Queries with constraints

### Select query with constraints

```sql
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;
```

#### Numbers Operators

<table><thead><tr><th width="220.79998779296875">Operator</th><th>Condition</th><th>SQL Example</th></tr></thead><tbody><tr><td>=, !=, &#x3C;, &#x3C;=, >, >=</td><td>Standard numerical operators</td><td>col_name != 4</td></tr><tr><td>BETWEEN … AND …</td><td>Number is within range of two values (inclusive)</td><td>col_name BETWEEN 1.5 AND 10.5</td></tr><tr><td>NOT BETWEEN … AND …</td><td>Number is not within range of two values (inclusive)</td><td>col_name NOT BETWEEN 1 AND 10</td></tr><tr><td>IN (…)</td><td>Number exists in a list</td><td>col_name IN (2, 4, 6)</td></tr><tr><td>NOT IN (…)</td><td>Number does not exist in a list</td><td>col_name NOT IN (1, 3, 5)</td></tr></tbody></table>

#### Character Operators

<table><thead><tr><th width="116">Operator</th><th width="356.599853515625">Condition</th><th>Example</th></tr></thead><tbody><tr><td>=</td><td>Case sensitive exact string comparison (<em>notice the single equals</em>)</td><td>col_name = "abc"</td></tr><tr><td>!= or &#x3C;></td><td>Case sensitive exact string inequality comparison</td><td>col_name != "abcd"</td></tr><tr><td>LIKE</td><td>Case insensitive exact string comparison</td><td>col_name LIKE "ABC"</td></tr><tr><td>NOT LIKE</td><td>Case insensitive exact string inequality comparison</td><td>col_name NOT LIKE "ABCD"</td></tr><tr><td>%</td><td>Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)</td><td>col_name LIKE "%AT%"<br>(matches "AT", "ATTIC", "CAT" or even "BATS")</td></tr><tr><td>_</td><td>Used anywhere in a string to match a single character (only with LIKE or NOT LIKE)</td><td>col_name LIKE "AN_"<br>(matches "AND", but not "AN")</td></tr><tr><td>IN (…)</td><td>String exists in a list</td><td>col_name IN ("A", "B", "C")</td></tr><tr><td>NOT IN (…)</td><td>String does not exist in a list</td><td>col_name NOT IN ("D", "E", "F")</td></tr></tbody></table>

## SQL Lesson 4: Filtering and sorting Query results

### Select query with unique results

```sql
// Some codeSQL
```

|   |   |   |
| - | - | - |
|   |   |   |
|   |   |   |
|   |   |   |
