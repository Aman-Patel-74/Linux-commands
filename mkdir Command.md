 mkdir Command

The `mkdir` command is used to create directories.

 Basic Usage:

- `mkdir directory_name`
    Creates a directory with the specified name.
    
    
    
    mkdir my_directory
    

Options:

- `-p` (parents)
    Creates parent directories as needed. If the specified directory already exists, no error is reported.
    
    
    mkdir -p /path/to/my_directory
    

- `-v` (verbose)
    Prints a message for each created directory.
    
    
    mkdir -v my_directory
    

Examples:

- To create a single directory:
    
    
    mkdir my_directory
    

- To create a directory and its parent directories:
    
    
    mkdir -p /path/to/my_directory
    

- To create a directory and print a message:
    
    
    mkdir -v my_directory
    