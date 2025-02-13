Default File Permission Calculation

# Understanding umask
The default file permissions in Linux are determined by the `umask` (user file creation mask). The `umask` sets the default permissions for newly created files and directories by masking out certain permission bits.

# Default Permissions
- Files: The base default permission is `666` (read and write for everyone).
- Directories: The base default permission is `777` (read, write, and execute for everyone).

# How umask Works
The `umask` value is subtracted from the base default permissions to determine the final default permissions.

# Example umask Values
- umask 022:
  - Files: `666 - 022 = 644` (rw-r--r--)
  - Directories: `777 - 022 = 755` (rwxr-xr-x)
- umask 027:
  - Files: `666 - 027 = 640` (rw-r-----
  - Directories: `777 - 027 = 750` (rwxr-x---)
- umask 077:
  - Files: `666 - 077 = 600` (rw-------
  - Directories: `777 - 077 = 700` (rwx------)

# Viewing and Setting umask
- View Current umask:
  
  umask
  
- Set umask:
  
  umask 022
  

# Example Commands
- View Current umask:
  
  umask
  
- Set umask to 027:
  
  umask 027
  

Understanding how `umask` works is essential for controlling the default permissions of newly created files and directories in a Linux environment.
