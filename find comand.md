find

GitHub Copilot: The `find` command is used in Windows to search for a specific text string in files. Here are some common switches and their descriptions:

- `/v` : Displays all lines NOT containing the specified string.
- `/c` : Displays only the count of lines containing the string.
- `/n` : Displays line numbers with the displayed lines.
- `/i` : Ignores the case of characters when searching for the string.

Syntax
plaintext
find [switches] "string" [pathname(s)]


Examples
1.Find a string in a file:**
   plaintext
   find "searchString" filename.txt
   

2.Find a string in all `.txt` files in a directory:**
   plaintext
   find "searchString" *.txt
   

3.Count the number of lines containing the string:**
   plaintext
   find /c "searchString" filename.txt
   

4.Find a string in a file, ignoring case:**
   plaintext
   find /i "searchString" filename.txt
   

5.Display lines not containing the string:**
   plaintext
   find /v "searchString" filename.txt
   