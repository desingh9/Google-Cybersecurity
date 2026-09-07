# **Exemplar: Find files with Linux commands**

## **Scenario**

In this scenario, you have to locate and analyze the information of certain files located in the */home/analyst* directory

Here’s how you’ll do this: **First**, you’ll get the information of the current working directory you’re in and display the contents of the directory. **Second**, you’ll navigate to the *reports* directory and list the subdirectories it contains. **Third**, you’ll navigate to the *users* subdirectory and display the contents of the *Q1\_added\_users.txt file*. **Finally**, you’ll navigate to the *logs* directory and display the first 10 lines of a file it contains. 

## **Task 1\. Get the current directory information**

In this task, you must use the commands you learned about to check the current working directory and list its contents.

1. Display your working directory.

The command to complete this step:

pwd

1

This will show that your current working directory is your home directory.

/home/analyst

2\. Display the names of the files and directories in the current working directory.

The command to complete this step:

ls

The output should be:

logs  projects  reports  temp  
Which directory is your current working directory?   
**Answer:** The lab starts with /home/analyst as your current working directory. 

## **Task 2\. Change directory and list the subdirectories**

In this task, you must navigate to a new directory and determine the subdirectories it contains.

1. Navigate to the /home/analyst/reports directory.

The command to complete this step using a relative path:

cd reports  
The command to complete this step using an absolute path:   
cd /home/analyst/reports  
2\. Display the files and subdirectories in the /home/analyst/reports directory.   
The command to complete this step:   
ls  
The output should be: 

users

Test the knowledge

### **1\.**Question 1

What does the term "command" mean?

1. An instruction instructing a computer to execute a specific task  
2. A fundamental element of the Linux system architecture  
3. The top-level root directory within a Linux file system  
4. A standard command-line shell utilized in Linux environments

### **2\.Question 2**

Which command is used to display the current working directory path on the screen?

1. *pwd*  
2. *ls*  
3. *cat*  
4. *head*

### **3\.Question 3**

What is the function of the *cd* command?

1. Navigates between directories  
2. Prints the working directory to the screen  
3. Displays the names of files in the current directory  
4. Outputs a specified string of text

