`sestatus` is a command in Linux used to display the current status of SELinux (Security-Enhanced Linux). SELinux is a security module that provides a mechanism for supporting access control security policies.

### Usage
To check the status of SELinux, simply run:
```sh
sestatus
```

### Output
The output of `sestatus` typically includes:
- **SELinux status**: Indicates whether SELinux is enabled or disabled.
- **SELinuxfs mount**: Shows the mount point of the SELinux filesystem.
- **Current mode**: Indicates the current mode of SELinux (enforcing, permissive, or disabled).
- **Mode from config file**: Shows the mode specified in the SELinux configuration file.
- **Policy version**: Displays the version of the SELinux policy.
- **Policy from config file**: Indicates the policy specified in the configuration file.

### Example Output
```plaintext
SELinux status:                 enabled
SELinuxfs mount:                /sys/fs/selinux
SELinux root directory:         /etc/selinux
Loaded policy name:             targeted
Current mode:                   enforcing
Mode from config file:          enforcing
Policy MLS status:              enabled
Policy deny_unknown status:     allowed
Max kernel policy version:      31
```

This command is useful for quickly checking the state and configuration of SELinux on a system.