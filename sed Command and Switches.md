sed Command and Switches

The `sed` command is a stream editor used to perform basic text transformations on an input stream (a file or input from a pipeline).

 Common Options:

- `-e` (script)
    Allows you to add the script to the commands to be executed.
    
    
    sed -e 's/old/new/' file.txt


- `-i` (in-place)
    Edits files in place (makes backup if extension is supplied).
    
    
    sed -i 's/old/new/' file.txt


- `-n` (quiet, silent)
    Suppresses automatic printing of pattern space. Useful when you only want to print specific lines.
    
    
    sed -n 'p' file.txt


- `-f` (file)
    Adds the script contained in the file to the commands to be executed.
    
    
    sed -f script.sed file.txt


- `-r` (extended regex)
    Uses extended regular expressions in the script.
    
    
    sed -r 's/(old|new)/replacement/' file.txt


- `-s` (separate)
    Treats files as separate rather than as a single continuous long stream.
    
    
    sed -s 's/old/new/' file1.txt file2.txt

    This documentation provides a brief description of the sed command and its common options, along with example usage for each option. This documentation provides a brief description of the sed command and its common options, along with example usage for each option.