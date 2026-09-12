# **Exemplar: Get help in the command line**

## **Activity Overview**

As a security analyst, knowing where to find answers is essential even if you don't know everything offhand. Fortunately, Linux allows you to access help documentation directly from the command line.

Discovering which commands to utilize and understanding their functionality is an invaluable skill in security analysis. To support this, the lab covers three key commands:

* **man**: Access comprehensive manual pages for detailed command information.  
* **whatis**: Display quick, single-line descriptions of command functions.  
* **apropos**: Search manual pages for commands matching a specific search string.

Keeping these tools in mind, let’s move on to the scenario.

## **Scenario Overview**

In this scenario, you will gather additional details about necessary commands and determine which specific command is required to complete a given task.

To complete this task, you will follow these steps:

1. **1\. Explore shell help commands:** Examine standard commands used in the shell to gather information about other utilities.  
2. **2\. Locate a command option:** Identify the required flag or option needed to modify a command's behavior.  
3. **3\. Compare command summaries:** Generate concise command descriptions to analyze their differences.

**4\. Select the appropriate command:** Determine the exact command suited for performing the target task.

## **Task 1\. Learn more about commands**

**First**, imagine you can’t quite remember what the *cat* command does and want a quick reminder.&nbsp;

Run the *whatis* command to get a short description of *cat*

whatis cat

&nbsp;

**Next**, imagine that you want more details about *cat* and all of its options.

1. Use the *man* command to get more details about *cat*.

The command to complete this step:

man cat

Running *man* provides an extensive summary of *cat* alongside details regarding every available flag:

&nbsp;

3\. Press **Q** to exit this manual page.

**Now**, imagine you’ve remembered there’s a command that prints just the first part of a file, but you can’t remember the exact command. The *apropos* command is useful in these instances. You can use keywords with *apropos* to find a command.

. . Use *apropos* to find a command that returns the first part of a file:&nbsp;

apropos \-a first part file

Which command returns the first part of a file?

**Answer**: The *head* command returns only the first part of a file.

## **Task 2\. Explore the useradd command**

In this task, imagine that you want to set the expiration date for a temporary user account. You know that you need to use the *useradd* command for this, but you’re not quite sure how to complete the task. You realize it might involve adding an option to the command.&nbsp;

Which command returns the first part of a file?

**Answer**: The *head* command returns only the first part of a file.

&nbsp;