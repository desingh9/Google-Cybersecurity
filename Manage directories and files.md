# **Manage directories and files**

In a previous lesson, you explored file system management using Linux commands. The commands covered were: *mkdir*, *rmdir*, *touch*, *rm*, *mv*, and *cp*. This reading provides a review of these Linux utilities, introduces the nano text editor, and demonstrates an additional method for writing content to files.

## **Creating and modifying directories**

### **mkdir**

The *mkdir* command creates a new directory. Like all of the commands presented in this reading, you can either provide the new directory as the absolute file path, which starts from the root, or as a relative file path, which starts from your current directory.

For example, if you want to create a new directory called *network* in your */home/analyst/logs* directory, you can enter *mkdir /home/analyst/logs/network* to create this new directory. If you’re already in the */home/analyst/logs* directory, you can also create this new directory by entering *mkdir network*.

**Pro Tip**: You can use the *ls* command to confirm the new directory was added.

### **rmdir**

The *rmdir* command removes, or deletes, a directory. For example, entering *rmdir /home/analyst/logs/network* would remove this empty directory from the file system.

**Note**: The *rmdir* command cannot delete directories with files or subdirectories inside. For example, entering *rmdir /home/analyst* returns an error message. 

## **Creating and modifying files**

### **touch and rm**

The *touch* command creates a new file. This file won’t have any content inside. If your current directory is */home/analyst/reports*, entering *touch permissions.txt* creates a new file in the *reports* subdirectory called *permissions.txt*.

The *rm* command removes, or deletes, a file. This command should be used carefully because it’s not easy to recover files deleted with *rm*. To remove the permissions file you just created, enter *rm permissions.txt*. 

**Pro Tip:** You can verify that *permissions.txt* was successfully created or removed by entering *ls*.

### **mv and cp**

When managing files, the *mv* and *cp* commands allow you to move and copy files or directories. Both commands take two main arguments: first, the target file or directory, followed by the destination path.

**Moving Files (*mv*)**

* The *mv* command transfers a file or directory to a new location, removing it from the source location.  
* Example: Execute *mv permissions.txt /home/analyst/logs* to relocate *permissions.txt* into the *logs* directory.

**Copying Files (*cp*)**

* The *cp* command duplicates a file or directory into a specified destination without deleting the original.  
* Example: Execute *cp permissions.txt /home/analyst/logs* to duplicate *permissions.txt* in the *logs* folder while keeping a copy in its initial location.

**Note**: The *mv* command can also be used to rename files. To rename a file, pass the new name in as the second argument instead of the new location. For example, entering *mv permissions.txt perm.txt* renames the *permissions.txt* file to *perm.txt*.

