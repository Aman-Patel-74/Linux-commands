passwd  to chge pass and other

The `passwd` command in Linux is used to change user passwords. Here are some common switches:

- `-d`: Delete a user's password (makes the account passwordless).
- `-e`: Expire a user's password immediately.
- `-i`: Set the number of days after a password expires until the account is disabled.
- `-l`: Lock a user's password.
- `-u`: Unlock a user's password.
- `-S`: Display account status information.

Example usage:

Change the password for the current user
passwd

Change the password for a specific user
sudo passwd username

Lock a user's password
sudo passwd -l username

Unlock a user's password
sudo passwd -u username

Expire a user's password immediately
sudo passwd -e username

Display account status information
passwd -S username
