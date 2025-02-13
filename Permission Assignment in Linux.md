Permission Assignment in Linux

# Symbolic Notation
Symbolic notation uses letters to represent permissions and operators to modify them.

 Syntax

chmod [who][operator][permission] filename


 Who
- `u`: User (owner)
- `g`: Group
- `o`: Others
- `a`: All (user, group, and others)

 Operators
- `+`: Adds a permission
- `-`: Removes a permission
- `=`: Sets the exact permission

 Permissions
- `r`: Read
- `w`: Write
- `x`: Execute

 Examples
- Add execute permission for the owner:
  
  chmod u+x filename
  
- Remove write permission for the group:
  
  chmod g-w filename
  
- Set read-only permission for others:
  
  chmod o=r filename
  

# Numeric Notation
Numeric notation uses octal numbers to represent permissions.

 Syntax

chmod [mode] filename


 Mode
Each permission is represented by a digit from 0 to 7:
- `4`: Read (`r`)
- `2`: Write (`w`)
- `1`: Execute (`x`)

Combine these values to set multiple permissions:
- `7` (4+2+1): Read, write, and execute (`rwx`)
- `6` (4+2): Read and write (`rw-`)
- `5` (4+1): Read and execute (`r-x`)
- `4`: Read only (`r--`)
- `3` (2+1): Write and execute (`-wx`)
- `2`: Write only (`-w-`)
- `1`: Execute only (`--x`)
- `0`: No permissions (`---`)

 Examples
- Set permissions to `rwxr-xr-x` (755)

  chmod 755 filename
  
- Set permissions to `rw-r--r--` (644):
  
  chmod 644 filename
  

# Example Commands
- **Add execute permission for the owner**:
  
  chmod u+x filename
  
- **Set permissions to `rwxr-xr-x`**:
  
  chmod 755 filename
  

Understanding both symbolic and numeric notations is essential for managing file permissions effectively in a Linux environment.
