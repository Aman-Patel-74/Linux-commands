Special Permissions in Linux

In addition to the standard read, write, and execute permissions, Linux supports special permissions that provide additional security and functionality.

#etuid (Set User ID)
- Symbol: `s` in the user execute position.
- Numeric: `4` (e.g., `4755`).
- Purpose: When set on an executable file, this permission allows the file to be executed with the privileges of the file owner, rather than the user running the file. This is commonly used for programs that need to perform tasks requiring higher privileges.
- Example: 
  
  chmod u+s filename
  
- Viewing: 
  
  ls -l filename
  
  Output:
  plaintext
  -rwsr-xr-x 1 owner group 4096 Jan 1 12:34 filename
  

# Setgid (Set Group ID)
- Symbol: `s` in the group execute position.
- Numeric: `2` (e.g., `2755`).
- Purpose: When set on an executable file, this permission allows the file to be executed with the privileges of the file's group. When set on a directory, new files and subdirectories created within inherit the group ID of the directory, rather than the primary group of the user who created the file.
- Example: 
  
  chmod g+s directory
  
- Viewing: 
  
  ls -l directory
  
  Output:
  plaintext
  drwxr-sr-x 2 owner group 4096 Jan 1 12:34 directory
  

# Sticky Bit
- Symbol: `t` in the others execute position.
- Numeric: `1` (e.g., `1755`).
- Purpose: When set on a directory, this permission restricts file deletion; only the file owner, the directory owner, or the root user can delete or rename the files within the directory. This is commonly used on directories like `/tmp` to prevent users from deleting each other's files.
- Example: 
  
  chmod +t directory
  
- Viewing: 
  
  ls -l directory
  
  Output:
  plaintext
  drwxr-xr-t 2 owner group 4096 Jan 1 12:34 directory
  

# Examples
- Setuid: 
  
  chmod 4755 filename
  
- Setgid: 
  
  chmod 2755 directory
  
- Sticky Bit: 
  
  chmod 1755 directory
  

# Viewing Special Permissions
Use `ls -l` to view special permissions:

ls -l

- Setuid: `-rwsr-xr-x`
- Setgid: `-rwxr-sr-x`
- Sticky Bit: `-rwxr-xr-t`

Understanding and using special permissions is crucial for managing security and functionality in a Linux environment.
