# **Exemplar: Perform an SQL query**

## **Activity overview**

Previously, you learned how to use basic SQL queries to retrieve information from a database. You have also learned about using the ORDER BY keyword to sort data returned in an ascending or a descending order.

## **Scenario**

In this scenario, you have to determine which employee devices must be updated. You also need to investigate user login activity to explore if any unusual activity has occurred.

The information you need is located in the *machines* and *login\_attempts* tables in the *organization* database.

The **machines** table focuses on hardware and includes these columns:

* **device\_id**  
* **operating\_system**  
* **email\_client**  
* **OS\_patch\_date**  
* **employee\_id**

The **log\_in\_attempts** table focuses on user activity and includes this columns:

* **event\_id**  
* **username**  
* **Login\_date**  
* **login\_time**  
* **country**  
* **ip\_address**  
* **success**

Here’s how you’ll do this task: First, you’ll obtain information on the employee devices that must be updated. Next, you’ll examine the login attempts for unusual activity. Finally, you’ll use the ORDER BY keyword to sort the data returned by your SQL queries.

OK, let’s get ready to practice running your very first SQL queries\!&nbsp;

## **Task 1: Accessing Employee Device Records**

In this task, you need to obtain information on employee devices because your team needs to update them. The information you need is in the *machines* table in the *organization* database.

**First**, you need to retrieve all the information about the employee devices.

1. Run the following query to select all device information from the *machines* table

SELECT \*

FROM machines;

Think of a SQL query like a sentence you are saying to the database:

* **SELECT:** "Which columns (specific details) do I want to see?"  
* **FROM:** "Which table are they stored in?"  
* **The Semicolon (;):** Think of this as the "period" at the end of your sentence. It tells the database, "I'm done talking, now run this\!"&nbsp;

***Note:** Using the asterisk (\*) returns all data from the specified table. Also, table names in MySQL are case-sensitive.*

The output returns all the contents of the *machines* table:

&nbsp;

```
+--------------+------------------+----------------+---------------+-------------+
| device_id    | operating_system | email_client   | OS_patch_date | employee_id |
+--------------+------------------+----------------+---------------+-------------+
| a184b775c707 | OS 1             | Email Client 1 | 2021-09-01    |        1156 |
| a192b174c940 | OS 2             | Email Client 1 | 2021-06-01    |        1052 |
| a305b818c708 | OS 3             | Email Client 2 | 2021-06-01    |        1182 |
| a317b635c465 | OS 1             | Email Client 2 | 2021-03-01    |        1130 |
| a320b137c219 | OS 2             | Email Client 2 | 2021-03-01    |        1000 |
|...           |                  |                |               |             |
+--------------+------------------+----------------+---------------+-------------+
200 rows in set (0.356 sec)
```

**Next**, you want to focus on the email client running on various devices.

2\. Run the following query to select only the *device\_id* and *email\_client* columns from the machines table.

**The Comma (***,***):** When selecting multiple columns (like *device\_id, email\_client*), the comma acts like a separator in a list. Notice there is **no comma** after the last item before the word *FROM*.

Replace *X* with *device\_id* and *Y* with *email\_client*:

*SELECT device\_id, email\_client FROM machines;*

The correct query to solve this step:&nbsp;

SELECT device\_id, email\_client

FROM machines;

The output should return only the selected columns of the machines table:&nbsp;

\+--------------+----------------+

| device\_id    | email\_client   |

\+--------------+----------------+

| a184b775c707 | Email Client 1 |

| a192b174c940 | Email Client 1 |

| a305b818c708 | Email Client 2 |

| a317b635c465 | Email Client 2 |

| a320b137c219 | Email Client 2 |

|...&nbsp;

\+--------------+----------------+

200 rows in set (0.015 sec)

What email client is returned in the third row?&nbsp;

**Answer**: The email client returned in the third row is Email Client 2\.&nbsp;

&nbsp;