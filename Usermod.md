Usermod

The `usermod` command in Linux is used to modify a user's account details. Here are some common switches (options) used with `usermod`:

- `-l`: Change the login name of the user.
- `-d`: Change the user's home directory.
- `-m`: Move the user's home directory to a new location.
- `-s`: Change the user's login shell.
- `-L`: Lock the user's account.
- `-U`: Unlock the user's account.
- `-G`: Add the user to supplementary groups.
- `-aG`: Append the user to supplementary groups without removing them from other groups.
- `-e`: Set the account expiration date.
- `-f`: Set the number of days after a password expires until the account is permanently disabled.
- `-u`: Change the user ID (UID) of the user.

Examples

1.Change the login name of a user:**
  
   sudo usermod -l newusername oldusername


2.Change the user's home directory:**
  
   sudo usermod -d /new/home/directory -m username


3.Change the user's login shell:**
  
   sudo usermod -s /bin/bash username


4.Lock a user's account:**
  
   sudo usermod -L username


5.Unlock a user's account:**
  
   sudo usermod -U username


6.Add a user to supplementary groups:**
  
   sudo usermod -aG group1,group2 username


7.Set the account expiration date:**
  
   sudo usermod -e YYYY-MM-DD username


8.Change the user ID (UID) of a user:**
  
   sudo usermod -u 1001 username


These commands allow you to manage user accounts effectively on a Linux system.