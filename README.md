# File Permissions in Linux

Project Description:

My organization's research team needs to adjust the file permissions for specific files and directories in the "project" directory.  The current permissions do not reflect the appropriate level of authorization.  Checking and upgrading these permissions will assist to keep their system secure.  To finish this challenge, I completed the following tasks:

Check file and directory details

The code below shows how I used Linux commands to determine the current permissions for a certain directory in the file system.

![image alt](https://github.com/mruiz4241/mruiz4241/blob/86832b390e8c2354bde768e0e86a11bba72f33bb/Screenshot%201.png)

The first line in the screenshot shows the command I entered, while the remaining lines show the output.  The code lists the whole contents of the project directory.  I ran the "ls" command with the "-la" option to get a complete list of the file contents, which included hidden files.  My command produced the following output: one directory entitled "drafts", one hidden file named ".project_x.txt", and five other project files.  The 10-character string in the first column represents the permissions assigned to each file or directory.
