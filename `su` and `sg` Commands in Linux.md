`su` and `sg` Commands in Linux

# `su` Command
The `su` (substitute user) command allows you to switch to another user account in the current session.

 Basic Syntax

su [options] [username]


 Common Options (Switches)
- `-`: Switch to the target user's environment.
  
  su - username
  
- `-c`: Run a specific command as the target user.
  
  su -c "command" username
  
- `-s`: Specify a shell to use.
  
  su -s /bin/bash username
  

 Examples
- Switch to root user:
  
  su -
  
- Switch to another user:
  
  su username
  
- Run a command as another user:
  
  su -c "ls /root" root
  

# `sg` Command
The `sg` (substitute group) command allows you to execute commands with a different group ID.

 Basic Syntax

sg [options] group


 Common Options (Switches)
- `-c`: Run a specific command with the specified group.
  
  sg group -c "command"
  

 Examples
- Run a command with a different group:
  
  sg groupname -c "command"
  

# Example Commands
- Switch to root user:
  
  su -
  
- Run a command as another user:
  
  su -c "ls /root" root
  
- Run a command with a different group:
  
  sg groupname -c "command"
  

Understanding the `su` and `sg` commands and their switches is essential for managing user and group permissions in a Linux environment.
