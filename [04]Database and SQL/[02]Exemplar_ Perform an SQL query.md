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

&nbsp;

&nbsp;