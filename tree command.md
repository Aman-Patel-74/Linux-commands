tree
The `tree` command in Linux is used to display the contents of a directory in a tree-like format. It recursively lists all files and directories in the specified directory.

 Basic Usage

tree [options] [directory]


 Common Options
- `-a`: All files are listed.
- `-d`: List directories only.
- `-L level`: Max display depth of the directory tree.
- `-f`: Print the full path prefix for each file.
- `-h`: Print the size of each file in a more human-readable way.
- `-I pattern`: Do not list files that match the pattern.

 Examples
1. Display the directory tree of the current directory:
 
   tree
   

2. Display the directory tree including hidden files:
 
   tree -a
   

3. Display directories only:
 
   tree -d
   

4. Limit the depth of the directory tree to 2 levels:
 
   tree -L 2
   

5. Display the full path for each file:
 
   tree -f
   

6. Display the size of each file in a human-readable format:
 
   tree -h
   

7. Exclude files matching a pattern (e.g., exclude `.git` directories):
 
   tree -I '.git'
   

 Getting Help
To get more information about the `tree` command and its options, you can use the `--help` option:
sh
tree --help
