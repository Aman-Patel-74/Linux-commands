cat


The cat (concatenate) command in Linux is a versatile and widely used command for displaying the content of files, combining multiple files, and even creating new files. It reads the content of files sequentially, writes them to standard output, and is especially helpful for viewing the contents of text files.
Syntax:

cat [options] file...

    file: The file or files whose contents you want to display or concatenate.

Basic Usage:

    Display the content of a file:

cat file.txt

    This will output the contents of file.txt to the terminal.

Concatenate multiple files:

cat file1.txt file2.txt

    This displays the contents of file1.txt followed by the contents of file2.txt in sequence.

Create a new file:

cat > newfile.txt

    This command allows you to type text directly into newfile.txt. To finish, press Ctrl+D to save and exit.

Append content to an existing file:

    cat >> existingfile.txt

        This allows you to append new content to existingfile.txt. Again, press Ctrl+D to save and exit.

Commonly Used Options for cat:

    -n (number lines)
        Displays line numbers before each line of the output. This is useful when you need to display and reference the lines of a file.

cat -n file.txt

-b (number non-empty lines)

    Numbers only the non-empty lines in the file, skipping blank lines.

cat -b file.txt

-E (show $ at the end of each line)

    Displays a $ symbol at the end of each line to visualize line endings, especially helpful when working with files that contain whitespace at the end of lines.

cat -E file.txt

-T (show TAB characters as ^I)

    Displays all TAB characters as ^I, helping to make tabs visible in a file.

cat -T file.txt

-A (show all non-printing characters)

    Combines -vET to display non-printing characters, tabs, and end-of-line markers. It’s useful when you need to inspect files that may contain invisible or special characters.

cat -A file.txt

-v (show non-printing characters)

    Displays non-printing characters except for tabs and line endings. It’s helpful to see control characters that are not normally displayed in files.

cat -v file.txt

--help

    Displays help information for the cat command, listing available options and how to use them.

cat --help

--version

    Displays the version of the cat command installed on the system.

    cat --version

Examples of cat Command Usage:

    Display the content of a single file:

cat file.txt

    Outputs the entire content of file.txt to the terminal.

Concatenate and display multiple files:

cat file1.txt file2.txt

    Outputs the contents of both file1.txt and file2.txt, one after the other.

Create a new file and input text:

cat > newfile.txt

    Allows you to enter content into newfile.txt by typing directly into the terminal. To save and exit, press Ctrl+D.

Append content to an existing file:

cat >> existingfile.txt

    Appends input text to existingfile.txt. Again, use Ctrl+D to save and exit.

Display line numbers for each line of a file:

cat -n file.txt

    Displays file.txt with line numbers for each line.

Display non-empty lines with numbers:

cat -b file.txt

    Displays file.txt but numbers only the non-empty lines.

Show $ at the end of each line:

cat -E file.txt

    Shows a $ symbol at the end of every line, useful for identifying trailing spaces.

Show special characters like TAB as ^I:

cat -T file.txt

    Displays TAB characters as ^I so you can visually inspect their presence.

Show all non-printing characters:

    cat -A file.txt

        Displays all control characters, spaces, and tabs in the file.

Additional Help Options:

    --help
        Provides a summary of options and how to use the cat command.

cat --help

man cat

    Displays the manual page for the cat command, providing detailed documentation on its usage and options.

    man cat

Conclusion:

    The cat command is a fundamental utility in Linux for viewing, combining, and creating files.
    Options like -n, -b, -E, and -v make it easy to manipulate and visualize the content of text files, especially when working with large datasets or files with non-printing characters.
    cat is often combined with other commands in pipelines to perform more complex tasks, making it one of the most versatile commands in Linux.

The echo command in Linux is used to display a line of text or a variable's value to the terminal or to a file. It is one of the most commonly used commands, as it helps with printing output, debugging, and controlling shell behavior. You can use echo to output messages, display variable values, and format text in various ways.
Syntax: