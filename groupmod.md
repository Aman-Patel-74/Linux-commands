The `groupmod` command in Linux is used to modify an existing group. Here are some common switches:

- `-g GID`: Change the group ID to the specified GID.
- `-n NEW_GROUP_NAME`: Change the name of the group to the specified new name.
- `-o`: Allow using a non-unique GID.

Example usage:
# Change the GID of the group 'developers' to 1002
sudo groupmod -g 1002 developers

# Change the name of the group 'developers' to 'devteam'
sudo groupmod -n devteam developers

# Change the GID of the group 'developers' to 1002, allowing non-unique GID
sudo groupmod -g 1002 -o developers
