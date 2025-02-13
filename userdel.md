userdel

The `userdel` command in Linux is used to delete a user account and related files. Here are some common switches (options) used with `userdel`:

- `-r`: Remove the user's home directory and mail spool.
- `-f`: Force the removal of the user account, even if the user is currently logged in.

Examples

1.Delete a user account:**

   sudo userdel username


2.Delete a user account and remove the user's home directory and mail spool:**

   sudo userdel -r username


3.Force the deletion of a user account:**

   sudo userdel -f username


4.Force the deletion of a user account and remove the user's home directory and mail spool:**

   sudo userdel -r -f username


These commands allow you to manage user accounts effectively on a Linux system.