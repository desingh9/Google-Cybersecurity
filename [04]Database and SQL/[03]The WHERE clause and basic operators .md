# **The WHERE clause and basic operators**

&nbsp;

Earlier, you learned how to use the *WHERE* clause to filter SQL query results. This reading covers how to use the *WHERE* clause, the *LIKE* operator, and the percent sign (*%*) wildcard. You will also learn about the underscore (*\_*) wildcard, which gives you another way to filter your data.

## **How filtering helps**

As a security analyst, you often work with large, complex security logs. Filtering with SQL helps you quickly find the specific information you need.

For example, you can filter logs to view login attempts for a single user, check activity during a security event, or list devices running a specific app version.

## **WHERE**&nbsp;

To create a filter in SQL, you need to use the keyword *WHERE*. *WHERE* indicates the condition for a filter.

If you needed to email employees with a title of IT Staff, you might use a query like the one in the following example. You can run this example to examine what it returns:&nbsp;

1 SELECT firstname, lastname, title, email

2 FROM employees

3 WHERE title \= 'IT Staff';

&nbsp;

&nbsp;

\+-----------+----------+----------+------------------------+

| FirstName | LastName | Title    | Email                  |

\+-----------+----------+----------+------------------------+

| Robert    | King     | IT Staff | robert@chinookcorp.com |

| Laura     | Callahan | IT Staff | laura@chinookcorp.com  |

\+-----------+----------+----------+------------------------+

&nbsp;

Rather than returning all records in the *employees* table, this *WHERE* clause instructs SQL to return only those that contain *'IT Staff'* in the *title* column. It uses the equals sign (*\=*) operator to set this condition.

**Note:** You should place the semicolon (*;*) where the query ends. When you add a filter to a basic query, the semicolon is after the filter.&nbsp;&nbsp;

## **Filtering for patterns**

You can also filter based on a pattern. For example, you can identify entries that start or end with a certain character or characters. Filtering for a pattern requires incorporating two more elements into your *WHERE* clause:

* a wildcard&nbsp;  
* the *LIKE* operator

&nbsp;