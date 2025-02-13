The `gpasswd` command in Linux is used to administer `/etc/group` and `/etc/gshadow`. It allows you to manage group memberships and passwords. Here are some common switches:

- `-a USER`: Add a user to the group.
- `-d USER`: Remove a user from the group.
- `-r`: Remove the group password.
- `-R`: Restrict access to the group.
- `-A ADMIN`: Set the list of group administrators.
- `-M USER,...`: Set the list of group members.

Example usage:

# Add a user 'john' to the group 'developers'
sudo gpasswd -a john developers

# Remove a user 'john' from the group 'developers'
sudo gpasswd -d john developers

# Remove the password for the group 'developers'
sudo gpasswd -r developers

# Restrict access to the group 'developers'
sudo gpasswd -R developers

# Set 'admin' as the administrator of the group 'developers'
sudo gpasswd -A admin developers

# Set 'john' and 'jane' as members of the group 'developers'
sudo gpasswd -M john,jane developers
```