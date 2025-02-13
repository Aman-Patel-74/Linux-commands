`chacl`(ACL Command in Linux)

The `chacl` (change ACL) command is used to change the Access Control Lists (ACLs) of files and directories in Linux. ACLs provide a more flexible permission mechanism than the traditional Unix permission model.

#Basic Syntax

chacl [options] acl_spec file


#Common Options (Switches)
- `-b`: Remove all ACL entries.
  
  chacl -b filename
 
- `-d`: Set the default ACL for a directory.
  
  chacl -d acl_spec directory
 
- `-R`: Apply ACL recursively to all files and directories.
  
  chacl -R acl_spec directory
 
- `-l`: List the ACLs of the specified file or directory.
  
  chacl -l filename
 

#Examples
- Add an ACL entry for a user:

  chacl u::rwx,g::r-x,o::r-- filename
 
- Remove all ACL entries:
  
  chacl -b filename
 
- Set the default ACL for a directory:
  
  chacl -d u::rwx,g::r-x,o::r-- directory
 
- Apply ACL recursively to a directory and its contents:
  
  chacl -R u::rwx,g::r-x,o::r-- directory
 
- List the ACLs of a file:
  
  chacl -l filename
 

#Viewing ACLs
Use the `getfacl` command to view ACLs of files and directories.

##Syntax

getfacl [options] file


##Example
- View ACL of a file:
  
  getfacl filename
 

Understanding the `chacl` command and its switches is essential for managing complex permission requirements in a Linux environment.
