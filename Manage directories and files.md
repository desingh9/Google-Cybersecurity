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

## **nano text editor**

**nano** is a user-friendly, command-line text editor included by default across many Linux distributions, making it a popular choice for beginners and security professionals alike. It enables you to easily handle core file management tasks, including file creation and editing.

### **Opening and Creating Files**

* **Open an existing file:** Type *nano* followed by the filename while inside its directory. For instance, running *nano permissions.txt* inside */home/analyst/reports* opens *permissions.txt* for editing. If you are working from a different location, specify the full absolute file path instead.  
* **Create a new file:** Type *nano* followed by the desired new filename. For example, running *nano authorized\_users.txt* within */home/analyst/reports* generates *authorized\_users.txt* in that folder and immediately opens it in the editor.

### **Saving and Exiting**

Because nano does not automatically save your changes, you must manually save prior to closing.

* **Save file:** Press *Ctrl \+ O* and confirm the filename when prompted.  
* **Exit editor:** Press *Ctrl \+ X*.

**Note**: Vim and Emacs are also popular command-line text editors.

## **Standard output redirection**

### **Saving and Exiting Files**

Since nano does not autosave, changes must be saved manually before exiting the editor.

* **Save file:** Press *Ctrl \+ O* and press Enter to confirm the filename.  
* **Exit editor:** Press *Ctrl \+ X*.

**Note**: Other widely used command-line text editors include Vim and Emacs.

## **Standard output redirection**

Output redirection provides another approach for writing data to files. As covered earlier, **standard input** consists of data supplied to the operating system through the command line, whereas **standard output** is the response sent back by the OS via the terminal.

Additionally, **piping** using the pipe character (*|*) routes the standard output of one command to serve as standard input for another command.

### **Redirection Operators (\&gt; and \&gt;\&gt;)**

Besides the pipe operator, you can direct standard output directly to files using the single right angle bracket (*\&gt;*) and double right angle bracket (*\&gt;\&gt;*) operators.

When combined with the *echo* command, these operators write output to a file instead of displaying it on the screen:

* **Overwrite operator (*\&gt;*):** Replaces all existing content in the specified file. Exercise caution with *\&gt;*, as overwritten data cannot easily be recovered.  
* **Append operator (*\&gt;\&gt;*):** Appends new content to the end of the destination file without affecting existing text.

### **Example Usage**

If you are working within a directory that contains a file named *permissions.txt*:

* Running *echo "last updated date" \&gt;\&gt; permissions.txt* appends the string “last updated date” to the end of the file.  
* Running *echo "time" \&gt; permissions.txt* afterward replaces the entire file contents with “time”.

**Note:** If the specified target file does not already exist, both *\&gt;* and *\&gt;\&gt;* will automatically create it.

## **Key takeaways**

## **Key takeaways**

Knowing how to manage the file system in Linux is an important skill for security analysts. Useful commands for this include: *mkdir*, *rmdir*, *touch*, *rm*, *mv*, and *cp*. When security analysts need to write to files, they can use the nano text editor, or the *\>* and *\>\>* operators.

