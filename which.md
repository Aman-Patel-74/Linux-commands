which


GitHub Copilot: The `which` command is used on Unix-like operating systems to locate the executable file associated with a given command. However, since you are on a Windows machine, you can use the `where` command, which serves a similar purpose.

Here is how you can use the `where` command with its options:

```plaintext
where [options] <filename>

 Options:
- `/R <path>`: Recursively search starting at the specified path.
- `/Q`: Quiet mode, returns only the exit code.
- `/F`: Display the matched file's full path.

 Examples:
1. To locate a file named `example.txt`:
   plaintext
    where example.txt
   

2. To search recursively in a specific directory:
   plaintext
    where /R C:\Users example.txt
   

3. To display the full path of the matched file:
   plaintext
    where /F example.txt
   

For more help on the `where` command, you can use:
```plaintext
where /?
