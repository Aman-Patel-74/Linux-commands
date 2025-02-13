echo


echo [options] [string...]

    string...: The text or variables to be displayed. If no text is provided, echo will output a blank line.

Basic Usage:

    Display a simple message:

echo Hello, World!

    This will output:

    Hello, World!

Display a variable's value:

name="John"
echo Hello, $name!

    This will output:

    Hello, John!

Display multiple words:

echo "This is a test"

    This will output:

    This is a test

Redirect output to a file:

echo "Hello, World!" > file.txt

    This writes the string "Hello, World!" to file.txt. If file.txt already exists, its contents will be overwritten.

Append output to a file:

    echo "New line" >> file.txt

        This appends "New line" to file.txt.

Commonly Used Options for echo:

    -n (no trailing newline)
        By default, echo adds a newline character (\n) at the end of the output. The -n option suppresses this, so the output will not be followed by a new line.

echo -n "Hello"

    This will output:

    Hello

-e (enable interpretation of backslash escapes)

    Normally, echo does not interpret special characters (like \n, \t, etc.). The -e option enables the interpretation of backslash escapes (e.g., newline, tab).

echo -e "Hello\nWorld"

    This will output:

    Hello
    World

-E (disable interpretation of backslash escapes)

    Disables the interpretation of backslash escapes, even if -e is used in the command.

echo -E "Hello\nWorld"

    This will output:

    Hello\nWorld

--help

    Displays help information for the echo command, listing all available options and their usage.

echo --help

--version

    Displays the version of the echo command installed on the system.

    echo --version

Examples of echo Command Usage:

    Display a simple string:

echo "Hello, World!"

    This will output:

    Hello, World!

Display multiple words:

echo "Welcome to Linux"

    This will output:

    Welcome to Linux

Display the value of a variable:

name="Alice"
echo "Hello, $name!"

    This will output:

    Hello, Alice!

Suppress the newline at the end of output:

echo -n "No newline here"

    This will output:

    No newline here

Enable backslash escapes (e.g., newline, tab):

echo -e "First line\nSecond line"

    This will output:

    First line
    Second line

Append output to a file:

echo "Appended text" >> file.txt

    This appends "Appended text" to file.txt.

Redirect output to a file (overwriting):

echo "This will overwrite the file" > file.txt

    This overwrites file.txt with "This will overwrite the file".

Show backslash escapes (e.g., \n, \t, etc.):

echo -e "Tab:\tHello"

    This will output:

        Tab:    Hello

Additional Help Options:

    --help
        Displays a brief description of echo options and usage.

echo --help

man echo

    Displays the manual page for the echo command, providing detailed documentation about the command and its options.

    man echo

Conclusion:

    The echo command is an essential tool in Linux for outputting text, displaying variables, and controlling text formatting.
    Key options like -n, -e, and -E allow users to modify how the output is displayed, including the ability to add or suppress newline characters and enable or disable special characters.
    echo is frequently used in scripts, command-line output, and for debugging purposes.
    The command is simple but powerful, and with options like --help and --version, it is easy to access more information about its functionality.