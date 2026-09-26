# **Continuous learning in SQL**

## **Aggregate functions**

In SQL, **aggregate functions** are functions that perform a calculation over multiple data points and return the result of the calculation. The actual data is not returned.&nbsp;

There are various aggregate functions that perform different calculations:

* *COUNT* returns a single number that represents the number of rows returned from your query.  
* *AVG* returns a single number that represents the average of the numerical data in a column.  
* *SUM* returns a single number that represents the sum of the numerical data in a column.&nbsp;

### **Aggregate function syntax**

To use an aggregate function, place the keyword for it after the *SELECT* keyword, and then in parentheses, indicate the column you want to perform the calculation on.

For example, when working with the *customers* table, you can use aggregate functions to summarize important information about the table. If you want to find out how many customers there are in total, you can use the *COUNT* function on any column, and SQL will return the total number of records, excluding *NULL* values. You can run this query and explore its output:&nbsp;

&nbsp;

SELECT COUNT(firstname)

FROM customers;

&nbsp;

\+------------------+

| COUNT(firstname) |

\+------------------+

|               59     |

\+------------------+

&nbsp;