# File Permissions in Linux

### Project Description:

My organization's research team needs to adjust the file permissions for specific files and directories in the `"project"` directory.  The current permissions do not reflect the appropriate level of authorization.  Checking and upgrading these permissions will assist to keep their system secure.  To finish this challenge, I completed the following tasks:

### Check file and directory details

The code below shows how I used Linux commands to determine the current permissions for a certain directory in the file system.

![image alt](https://github.com/mruiz4241/mruiz4241/blob/86832b390e8c2354bde768e0e86a11bba72f33bb/Screenshot%201.png)

The first line in the screenshot shows the command I entered, while the remaining lines show the output.  The code lists the whole contents of the project directory.  I ran the `ls` command with the `"-la"` option to get a complete list of the file contents, which included hidden files.  My command produced the following output: one directory entitled `drafts`, one hidden file named `".project_x.txt"`, and five other project files.  The 10-character string in the first column represents the permissions assigned to each file or directory.

### Describe the permissions string

The 10-character string can be dissected to discover who has access to the file and with what permissions.  The characters signify the following:

* The first character, either a `d` or a hyphen (`-`), denotes the file type.  If the letter is `d`, it represents a directory.  A hyphen (`-`) indicates a normal file.
* The second through fourth characters represent the user's read (`r`), write (`w`), and execute (`x`) permissions.  When one of these characters is replaced with a hyphen (`-`), it means that the user does not have this permission.
* The fifth through seventh characters represent the group's read (`r`), write (`w`), and execute (`x`) permissions.  When one of these letters is a hyphen (`-`), it means that this permission is not granted to the group.
* The eighth through tenth characters indicate read (`r`), write (`w`), and execute (`x`) rights for others.  This owner type includes all other users on the system, excluding the user and group.  When one of these characters is a hyphen (`-`), it signifies that the permission is not granted to the other.

For example, `project_t.txt` has file permissions of `-rw-rw-r--`.  The initial character, a hyphen (`-`), indicates that project_t.txt is a file rather than a directory.  The second, fifth, and eighth characters are all `r`, indicating that the user, group, and other have read access.  The third and sixth characters, `w`, indicate that only the user and group have write rights.  No one has execute permissions on `project_t.txt`.

### Change file permissions

The organization decided that others should not have write access to any of their files.  To comply with this, I used the file permissions I had previously returned.  I determined `project_k.txt` must have the write access removed for other.

The following code demonstrates how I used Linux commands to do this:

