 ls Command and Switches

The `ls` command is used to list directory contents.

 Common Options:

- `-l` (long listing format)
    Displays detailed information about each file and directory.
    

    ls -l


  `-a` (all files)
    Lists all files, including hidden files (those starting with a dot).
    
    
    ls -a
    

- `-h` (human-readable)
    With `-l`, prints sizes in human-readable format (e.g., 1K, 234M, 2G).
    
    
    ls -lh
    

- `-R` (recursive)
    Lists subdirectories recursively.
    
    
    ls -R
    

- `-t` (sort by modification time)
    Sorts files by modification time, newest first.
    
    
    ls -t
    

- `-r` (reverse order)
    Reverses the order of the sort.
    
    
    ls -r
    

- `-S` (sort by file size)
    Sorts files by size, largest first.
    
    
    ls -S
    

- `-1` (one file per line)
    Lists one file per line.
    
    
    ls -1
    

Combining Options:

You can combine multiple options to customize the output. For example:


ls -lha