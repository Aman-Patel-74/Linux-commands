Linux permissions

 control who can read, write, or execute a file. Each file and directory has three types of permissions:

1.Read (r): Allows viewing the contents of the file.
2.Write (w): Allows modifying the contents of the file.
3.Execute (x): Allows running the file as a program.

Permissions are divided into three categories:

1.Owner: The user who owns the file.
2.Group: The group that owns the file.
3.Others: All other users.

You can view the permissions of a file using the `ls -l` command. For example:


ls -l filename


This might output something like:

plaintext
-rwxr-xr--


This means:
- `-`: It's a regular file.
- `rwx`: The owner has read, write, and execute permissions.
- `r-x`: The group has read and execute permissions.
- `r--`: Others have read permissions.

You can change permissions using the `chmod` command. For example:


chmod 755 filename


This sets the permissions to `rwxr-xr-x`.

You can also use symbolic notation with `chmod`:


chmod u+x filename  # Adds execute permission for the owner
chmod g-w filename  # Removes write permission for the group
chmod o=r filename  # Sets read-only permission for others


To change the owner of a file, use the `chown` command:


chown newowner filename


To change the group of a file, use the `chgrp` command:


chgrp newgroup filename



Here are the key points about Linux permissions:

1.Types of Permissions:
   -Read (r): View file contents.
   -Write (w): Modify file contents.
   -Execute (x): Run the file as a program.

2.Permission Categories:
   -Owner: User who owns the file.
   -Group: Group that owns the file.
   -Others: All other users.

3.Viewing Permissions:
   - Use `ls -l filename` to view permissions.

4.Changing Permissions:
   - Use `chmod` to change permissions.
     - Numeric notation: `chmod 755 filename`
     - Symbolic notation: `chmod u+x filename`

5.Changing Ownership:
   - Use `chown newowner filename` to change the owner.
   - Use `chgrp newgroup filename` to change the group.





   
 Linux Permissions and User/Group Management

 Linux Permissions

 Types of Permissions
1.Read (r): Allows viewing the contents of the file.
2.Write (w): Allows modifying the contents of the file.
3.Execute (x): Allows running the file as a program.

 Permission Categories
1.Owner: The user who owns the file.
2.Group: The group that owns the file.
3.Others: All other users.

 Viewing Permissions
- Use `ls -l filename` to view permissions.

 Changing Permissions
- Use `chmod` to change permissions.
  - Numeric notation: `chmod 755 filename`
  - Symbolic notation: `chmod u+x filename`

 Changing Ownership
- Use `chown newowner filename` to change the owner.
- Use `chgrp newgroup filename` to change the group.

 User Management

 Adding a User
- Use the `useradd` command to add a new user.
  
  sudo useradd username
  
- Set a password for the new user.
  
  sudo passwd username
  

 Deleting a User
- Use the `userdel` command to delete a user.
  
  sudo userdel username
  

 Modifying a User
- Use the `usermod` command to modify user properties.
  
  sudo usermod -aG groupname username  # Add user to a group
  

 Group Management

 Adding a Group
- Use the `groupadd` command to add a new group.
  
  sudo groupadd groupname
  

 Deleting a Group
- Use the `groupdel` command to delete a group.
  
  sudo groupdel groupname
  

 Modifying a Group
- Use the `gpasswd` command to administer group membership.
  
  sudo gpasswd -a username groupname  # Add user to group
  sudo gpasswd -d username groupname  # Remove user from group
  

 Viewing User and Group Information

 List Users
- View the `/etc/passwd` file.
  
  cat /etc/passwd
  

 List Groups
- View the `/etc/group` file.
  
  cat /etc/group
  

 Check User Groups
- Use the `groups` command to see which groups a user belongs to.
  
  groups username





  markdown
 Viewing Permissions

To view the permissions of a file or directory, use the `ls -l` command. This command lists the details of files and directories, including their permissions.

 Example

ls -l filename


 Output Explanation
The output of the `ls -l` command might look like this:
plaintext
-rwxr-xr--


This output can be broken down as follows:
- `-`: Indicates a regular file (a `d` would indicate a directory).
- `rwx`: The owner has read, write, and execute permissions.
- `r-x`: The group has read and execute permissions.
- `r--`: Others have read permissions.

 Detailed Breakdown
-First character: File type (`-` for regular file, `d` for directory, `l` for symbolic link, etc.).
-Next three characters: Owner permissions.
-Next three characters: Group permissions.
-Last three characters: Others permissions.

 Example Command
To view the permissions of all files in the current directory:

ls -l


