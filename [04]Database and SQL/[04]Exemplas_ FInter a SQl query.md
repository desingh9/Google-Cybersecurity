# **Exemplar: Filter a SQL query**

## **Scenario**

In this scenario, you need to get specific information about employees, their machines, and the departments they’re in. Your team needs this data to perform various tasks, such as running updates, posting a privacy notice in certain departments, and sending an alert to an employee with an issue on a machine.

You are responsible for finding the required information by querying a database. You’ll add filters to your queries to locate the information more quickly.

Here’s how you’ll do this task: **First**, you’ll list all organization machines and their operating systems. **Second**, you’ll list all machines with the operating system OS 2\. **Third**, you’ll list all the employees in the Finance and Sales departments. **Fourth**, you’ll obtain information about machines.

You’re ready to add filters to SQL queries.

*If you unintentionally exit the organization database in the MariaDB shell, you can reconnect by running the sudo mysql organization command.*&nbsp;

### **Orientation: Know Your Data**

Before you start querying, it is helpful to know exactly what the tables and columns look like. Run these two commands in your terminal to see the structure of the database:

*DESCRIBE machines;*&nbsp;

*DESCRIBE employees;*

What does *DESCRIBE* do? Think of *DESCRIBE* as a Table of Contents. It tells you exactly how a table is built without showing you all the rows of data. When you run it, you will see:

* Field: The exact name of the columns (e.g., *device\_id*). You must use these exact names in your SELECT statements.  
* Type: The kind of data allowed in that column (e.g., *int* for whole numbers or *varchar* for text).

You can run the *DESCRIBE* command at any time to refresh your memory on the column names for the tables.

## **task 1\. List all organization machines**

In this task, you need to get a list of all organization machines and their operating systems. The data is contained in the *machines* table. You’ll need to use the *SELECT* keyword to return specific columns.

* Run a SQL query to retrieve only the *device\_id* and *operating\_system* columns from the machines table.

The command to complete this step:

SELECT device\_id, operating\_system&nbsp;

FROM machines;

&nbsp;

The output lists only the selected columns from all the rows in the machines table:

200 rows in set (0.028 sec)

\+--------------+------------------+

|...                              |

\+--------------+------------------+

| device\_id    | operating\_system |

\+--------------+------------------+

| a184b775c707 | OS 1             |

| a192b174c940 | OS 2             |

| a305b818c708 | OS 3             |

| a317b635c465 | OS 1             |

| a320b137c219 | OS 2             |

| a398b471c573 | OS 3             |

&nbsp;

How many rows were returned from the machines table? (You can view the number of rows at the bottom of the output.)

**Answer**: The machines table returned 200 rows.

&nbsp;

&nbsp;