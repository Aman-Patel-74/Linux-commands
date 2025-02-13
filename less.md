less 

less Command in Linux – Detailed Summary

The less command in Linux is used to view the contents of files one page at a time. It allows you to scroll through the file using both forward and backward navigation, making it ideal for viewing long files. Unlike cat, which displays the entire content at once, less lets you interactively navigate through the content, providing better control when working with large files.
Syntax:

less [options] file

    file: The name of the file you want to view.

Basic Usage:

    View a file with less:

less file.txt

    Opens file.txt in the less pager, where you can scroll through the content.

View the contents of a large file:

    less largefile.txt

        Allows you to navigate through a large file without overwhelming the terminal output.

Commonly Used Options for less:

    -N (show line numbers)
        Displays line numbers on the left side of the file.

less -N file.txt

-S (chop long lines)

    By default, less wraps long lines. The -S option prevents this, so long lines will be chopped off at the edge of the terminal window.

less -S file.txt

-X (don't clear the screen)

    By default, less clears the screen when you exit. The -X option prevents the screen from being cleared.

less -X file.txt

-F (automatically exit if the content fits in one screen)

    If the content of the file can fit in one screen, less will display it and then exit automatically.

less -F file.txt

-i (ignore case in search)

    Makes the search case-insensitive.

less -i file.txt

--help

    Displays a list of options and their usage for less.

less --help

--version

    Displays the version information of the less command.

    less --version

Navigation in less:

    Move forward one page:
        Press Space or f.

    Move backward one page:
        Press b.

    Scroll up one line:
        Press the Up arrow key.

    Scroll down one line:
        Press the Down arrow key.

    Search for a string:
        Press / and type the search term, then press Enter.

    Go to the next search result:
        Press n.

    Go to the previous search result:
        Press N.

    Exit less:
        Press q.

Examples of less Command Usage:

    View a file with line numbers:

less -N file.txt

Scroll through a file without wrapping long lines:

less -S file.txt

Search for a keyword inside a file:

    less file.txt

        Then press / followed by the search term, e.g., /example.

    Exit less:
        Press q to quit viewing the file.

Additional Help Options:

    --help
        Displays a summary of available options and usage for less.

less --help

man less

    Displays the manual page for less, providing more detailed information.
