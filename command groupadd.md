command groupadd

 command in Linux is used to create a new group. This command is typically used by system administrators to manage user groups on a system. Here are some common options:

- `-f`: Exit with success status if the group already exists.
- `-g GID`: Specify the group ID for the new group.
- `-K KEY=VALUE`: Override `/etc/login.defs` defaults.
- `-o`: Allow creating a group with a non-unique GID.
- `-p PASSWORD`: Specify an encrypted password for the group.
- `-r`: Create a system group (with a GID less than 1000).

Example usage:

Create a new group named 'developers'
sudo groupadd developers

Create a new group with a specific GID
sudo groupadd -g 1001 developers

Create a system group
sudo groupadd -r sysgroup



