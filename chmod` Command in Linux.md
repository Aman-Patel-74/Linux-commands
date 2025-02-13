chmod` Command in Linux

The `chmod` command is used to change the file mode (permissions) of a file or directory.

#Basic Syntax
```sh
chmod [options] mode filename
```

#Modes
- Symbolic Notation: `chmod u+x filename`
- Numeric Notation: `chmod 755 filename`

#Common Options (Switches)
- `-R`: Recursively change permissions of directories and their contents.
 
  chmod -R 755 directory

- `-v`: Verbose mode, shows files as they are processed.
 
  chmod -v 755 filename

- `-c`: Like verbose but reports only when a change is made.
 
  chmod -c 755 filename

- `--reference=ref_file`: Set permissions to match those of `ref_file`.
 
  chmod --reference=ref_file filename


#Examples
- Add execute permission for the owner:
 
  chmod u+x filename

- Set permissions to `rwxr-xr-x`:
 
  chmod 755 filename

- Recursively change permissions of a directory and its contents:
 
  chmod -R 755 directory

- Verbose mode:
 
  chmod -v 644 filename


#Example Commands
- Add write permission for the group:
 
  chmod g+w filename

- Remove execute permission for others:
 
  chmod o-x filename

- Set permissions to match another file:
 
  chmod --reference=ref_file filename


Understanding the `chmod` command and its switches is crucial for managing file permissions effectively in a Linux environment.
```