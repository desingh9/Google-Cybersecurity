Navigate the Linux file system

*Welcome to module 3

Filesystem Hierarchy Standard (FHS)

Previously, you learned that the Filesystem Hierarchy Standard (FHS) is the component of Linux that organizes data. The FHS is important because it defines how directories, directory contents, and other storage is organized in the operating system.

This diagram illustrates the hierarchy of relationships under the FHS:

<img width="1600" height="659" alt="image" src="https://github.com/user-attachments/assets/2e9c2239-6d41-43e7-aa04-7ed69b41b899" />

Under the FHS, a file’s location can be described by a file path. A file path is the location of a file or directory. In the file path, the different levels of the hierarchy are separated by a forward slash (/).
Root directory

The root directory is the highest-level directory in Linux, and it’s always represented with a forward slash (/).  All subdirectories branch off the root directory. Subdirectories can continue branching out to as many levels as necessary.

Standard FHS directories

Directly below the root directory, you’ll find standard FHS directories. In the diagram, home, bin, and etc are standard FHS directories. Here are a few examples of what standard directories contain:

    /home: Each user in the system gets their own home directory.

    /bin: This directory stands for “binary” and contains binary files and other executables. Executables are files that contain a series of commands a computer needs to follow to run programs and perform other functions.

    /etc: This directory stores the system’s configuration files.

    /tmp: This directory stores many temporary files. The /tmp directory is commonly used by attackers because anyone in the system can modify data in these files.

    /mnt: This directory stands for “mount” and stores media, such as USB drives and hard drives.

Pro Tip: You can use the man hier command to learn more about the FHS and its standard directories.
