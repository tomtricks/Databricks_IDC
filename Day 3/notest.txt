PySpark vs Pandas Comparison
The fundamental difference lies in their approach to data size and execution: 
Pandas is designed for small-to-medium datasets that fit comfortably into a single machine's memory. It operates in-memory and is generally faster for these smaller, localized tasks.
PySpark (the Python API for Apache Spark) is built for large-scale, distributed computing. 
It processes data across a cluster of machines, making it ideal for "big data" scenarios where the dataset size exceeds the memory capacity of a single computer.
It achieves parallel processing through concepts like RDDs and DataFrames, ensuring scalability.

Joins (Inner, Left, Right, Outer)
Joins are used to combine two DataFrames (or tables) based on common columns (keys). The type of join determines which rows are kept: 
inner: Returns only rows that have matching keys in both DataFrames.
left (outer): Returns all rows from the left DataFrame and only matching rows from the right. Unmatched rows on the right are filled with null/NaN values.
right (outer): Returns all rows from the right DataFrame and only matching rows from the left. Unmatched rows on the left are filled with null/NaN values.
full (outer): Returns all rows when there is a match in either the left or the right DataFrame. Unmatched fields are filled with null/NaN values. 

Window Functions (Running Totals, Rankings)
Window functions perform calculations across a set of table rows that are related to the current row, unlike standard aggregate functions that collapse rows into a single result. They are powerful for analytical tasks: 
Running Totals: Calculating a cumulative sum of a column over a defined order of rows.
Rankings: Assigning ranks to rows based on a specific column's value (e.g., rank(), dense_rank(), row_number()). This is useful for tasks like finding the top 10 items in a category.
LEAD() and LAG(): Accessing data from subsequent or previous rows, respectively, useful for comparing current values to prior periods. 


User-Defined Functions (UDFs)
UDFs allow users to register custom Python functions (or other languages in Spark) as functions usable within DataFrame operations. 
Purpose: They are used when built-in functions do not cover the required custom logic or business rules.
Performance Consideration (PySpark): While flexible, UDFs in PySpark can be less efficient than built-in Spark functions because they often require data to be serialized back into Python processes for execution, breaking some of Spark's performance optimizations (like predicate pushdown). 
Built-in functions should always be preferred when available.
Performance Consideration (Pandas): In Pandas, apply() or vectorization are often used for custom logic, and performance is generally good within the single-machine context.

Hands-on
### Tasks:

1. Load full e-commerce dataset
2. Perform complex joins
3. Calculate running totals with window functions
4. Create derived features


![day 3 code image](day3-code.png)

#DatabricksWithIDC



