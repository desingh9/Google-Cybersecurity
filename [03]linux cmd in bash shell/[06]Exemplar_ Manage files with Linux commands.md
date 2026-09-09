# **Exemplar: Manage files with Linux commands**

## **Activity overview**

In this lab activity, you will modify a directory structure and its contents using Linux commands, as well as add text to a file using the nano text editor.

## **Scenario**

In this scenario, your objective is to ensure the proper organization of the */home/analyst* directory.

This involves making several updates to the */home/analyst* directory and its files, as well as updating a specific file to record all changes made.

At the start of the task, the initial structure of the */home/analyst* directory includes the following subdirectories and files:

home  
└── analyst  
    ├── notes  
    │   ├── Q3patches.txt  
    │   └── tempnotes.txt  
    ├── reports  
    │   ├── Q1patches.txt  
    │   └── Q2patches.txt  
    └── temp  
You need to modify the /home/analyst directory to the following directory and file structure:   
home  
└── analyst  
    ├── logs  
    ├── notes  
    │   └── tasks.txt      
    └── reports  
        ├── Q1patches.txt  
        └── Q2patches.txt  
        └── Q3patches.txt

You can accomplish this by following these steps:

1. **1\. Create the logs subdirectory:** Add a new *logs* subdirectory inside the */home/analyst* directory.  
2. **2\. Delete the temp subdirectory:** Remove the existing *temp* subdirectory.  
3. **3\. Relocate and clean up files:** Transfer the *Q3patches.txt* file into the *reports* subdirectory, then remove the *tempnotes.txt* file.  
4. **4\. Create a task log:** Generate a new *.txt* file named *tasks* within the *notes* subdirectory, and include a brief summary detailing the actions you completed.

This might sound like quite a number of tasks to perform, but you’ll be guided on how to do this. 

## **Task 1\. Create a new directory**

Begin by establishing a dedicated folder named *logs* to store all incoming log files.

1. Generate a new subdirectory titled *logs* within the */home/analyst* directory.  
   Run the following command to complete this action:  
1. mkdir logs  
2. Verify the creation of the *logs* subdirectory by listing the contents of */home/analyst*.  
   Run the following command to check the folder contents:  
   ls

The command output should display the original folders alongside the newly created *logs* subdirectory:

1. logs notes reports temp

## **Task 2\. Remove a directory**

Next, you must remove the *temp* directory, as you’ll no longer be placing items in it.

1. Remove the */home/analyst/temp* directory.

