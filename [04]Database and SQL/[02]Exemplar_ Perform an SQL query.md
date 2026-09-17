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

&nbsp;

&nbsp;