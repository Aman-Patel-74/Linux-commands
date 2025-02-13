

To customize the `/etc/default/useradd` file, follow these steps:

1. Open the file in a text editor:
   Use a text editor like `nano` or `vim` to open the file. For example, using `nano`:

   sudo nano /etc/default/useradd

2. Edit the file:
   Modify the parameters as needed. Here are some common parameters you might want to customize:
   - `GROUP`: Default group ID for new users.
   - `HOME`: Default base directory for new user home directories.
   - `INACTIVE`: Number of days after a password expires until the account is permanently disabled.
   - `EXPIRE`: Date on which the account will be disabled.
   - `SHELL`: Default login shell for new users.
   - `SKEL`: Directory containing default files for new user home directories.
   - `CREATE_MAIL_SPOOL`: Whether to create a mail spool file for new users.

   Example content:

   # Default values for useradd(8)
   GROUP=100
   HOME=/home
   INACTIVE=-1
   EXPIRE=
   SHELL=/bin/bash
   SKEL=/etc/skel
   CREATE_MAIL_SPOOL=yes

3. Save and close the file:
   If using `nano`, press `Ctrl+O` to save and `Ctrl+X` to exit.

4. Apply changes:
   The changes will be applied the next time you create a new user with the `useradd` command.

This allows you to set default values for new user accounts, streamlining the user creation process.