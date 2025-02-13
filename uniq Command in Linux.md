uniq Command in Linux 

The uniq command in Linux is used to filter out or remove duplicate lines from a sorted file. It can also be used to count occurrences of unique lines and output only those that appear a certain number of times. The uniq command is typically used in conjunction with the sort command, as it only works on sorted input.
Basic Syntax:

uniq [options] [input_file] [output_file]

    options: Flags that modify the behavior of uniq.
    input_file: The file from which to read input. If no file is provided, uniq reads from standard input (stdin).
    output_file: The file to write the result to (optional).

Common Options for uniq:

    -c (count)
        Precedes each unique line with the number of occurrences of that line.

uniq -c file.txt

    Example: Shows the frequency of each line in file.txt.

-d (duplicates)

    Only displays lines that are repeated (i.e., those that appear more than once).

uniq -d file.txt

    Example: Outputs only the lines in file.txt that appear more than once.

-u (unique)

    Only displays lines that are unique (i.e., those that appear exactly once).

uniq -u file.txt

    Example: Outputs only the lines in file.txt that appear exactly once.

-i (ignore case)

    Ignores case when comparing lines. This means lines that differ only in case are considered duplicates.

uniq -i file.txt

    Example: Treats "Hello" and "hello" as identical lines.

-f (fields)

    Skips the first n fields (columns) when comparing lines. Fields are defined by whitespace or a custom delimiter.

uniq -f 2 file.txt

    Example: Skips the first two fields of each line in file.txt when checking for uniqueness.

-s (skip)

    Skips the first n characters of each line before comparing.

uniq -s 3 file.txt

    Example: Skips the first three characters of each line in file.txt when checking for uniqueness.

-w (width)

    Compares only the first n characters of each line. This can be useful when only part of the line is relevant for comparison.

uniq -w 5 file.txt

    Example: Compares only the first 5 characters of each line in file.txt for uniqueness.

-z (NUL-terminated)

    Treats the input as NUL-terminated rather than newline-terminated. This can be useful for working with filenames or other data that may contain special characters.

uniq -z file.txt

    Example: Processes NUL-terminated input, often useful in scripts with filenames.

-h (help)

    Displays a help message showing all available options for the uniq command.

    uniq -h

        Example: Shows the help message for uniq.

Examples of uniq Command Usage:

    Remove Duplicates and Show the Result:

uniq file.txt

    Removes duplicate lines from file.txt and displays only unique lines.

Count Occurrences of Each Line:

uniq -c file.txt

    Displays each unique line from file.txt, preceded by the number of times it appears.

Display Only Duplicates (Lines that Appear More Than Once):

uniq -d file.txt

    Displays only the lines that appear more than once in file.txt.

Display Only Unique Lines (Lines that Appear Exactly Once):

uniq -u file.txt

    Displays only the lines that appear exactly once in file.txt.

Ignore Case While Removing Duplicates:

uniq -i file.txt

    Treats "apple" and "Apple" as the same line and removes duplicate entries, ignoring case.

Skip the First Field and Remove Duplicates:

uniq -f 1 file.txt

    Skips the first field (column) of each line and removes duplicates based on the remaining part of the line.

Skip the First Three Characters and Remove Duplicates:

uniq -s 3 file.txt

    Skips the first three characters of each line in file.txt and removes duplicates based on the rest of the line.

Compare Only the First 5 Characters for Uniqueness:

uniq -w 5 file.txt

    Compares only the first 5 characters of each line to determine uniqueness.

Process NUL-Terminated Input:

    uniq -z file.txt

        Processes NUL-terminated data in file.txt.

How to View the Help for uniq

    Using --help option:

uniq --help

    Displays a brief summary of available options for the uniq command.

Manual page (man): You can access detailed documentation using the man command:

    man uniq

Conclusion:

    The uniq command is an essential tool for filtering duplicate lines in a sorted file or input stream. It can be used to count the number of occurrences of each line, display only duplicates or unique lines, and customize the comparison criteria using various options.
    Common use cases include removing duplicate entries from text files, filtering logs, and counting occurrences of specific items.
    With options like -c (count), -d (duplicates), -u (unique), and -i (ignore case), uniq is a powerful utility for text processing in Linux.

