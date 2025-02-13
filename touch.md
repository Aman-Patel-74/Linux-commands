touch

reate an empty file:

touch file.txt

    This will create a file named file.txt if it does not exist. If it already exists, it updates the modification time (mtime) and access time (atime) to the current time.

Update the timestamp of an existing file:

touch existingfile.txt

    If existingfile.txt exists, it will update its access and modification times to the current system time.

Create multiple files:

    touch file1.txt file2.txt file3.txt

        This command creates file1.txt, file2.txt, and file3.txt if they do not already exist.

Commonly Used Options for touch:

    -a (access time only)
        Updates only the access time (atime) of the file, without changing the modification time.

touch -a file.txt

-m (modification time only)

    Updates only the modification time (mtime) of the file, without changing the access time.

touch -m file.txt

-c (no creation)

    This option prevents creating a file if it does not already exist. It only updates the timestamps of existing files.

touch -c file.txt

-t (set a custom timestamp)

    Allows you to specify a custom timestamp for the file. The timestamp format is:
    [[CC]YY]MMDDhhmm[.ss]
        CC: Century (optional).
        YY: Year (optional).
        MM: Month (two digits).
        DD: Day (two digits).
        hh: Hour (two digits).
        mm: Minute (two digits).
        ss: Second (two digits, optional).

touch -t 202401010800.30 file.txt

    This sets the timestamp of file.txt to January 1, 2024, 08:00:30 AM.

-d (date string)

    Sets the timestamp using a human-readable date string instead of the format used with -t.

touch -d "2024-01-01 08:00:30" file.txt

    This sets the timestamp of file.txt to January 1, 2024, 08:00:30 AM.

-r (reference file)

    Sets the timestamp of the current file to the timestamp of the reference file.

touch -r referencefile.txt file.txt

    This updates the timestamps of file.txt to match those of referencefile.txt.

-h (don't follow symlink)

    Modifies the symlink itself, not the file it points to.

touch -h symlink.txt

    This updates the timestamp of the symlink symlink.txt instead of the target file it points to.

--help

    Displays a summary of available options and usage for the touch command.

    touch --help

Examples of touch Command:

    Create an empty file:

touch newfile.txt

    Creates newfile.txt if it doesn't exist.

Update the timestamp of an existing file:

touch existingfile.txt

Create multiple files:

touch file1.txt file2.txt file3.txt

    Creates all three files if they don’t exist.

Update only the access time:

touch -a file.txt

Set a custom timestamp for a file:

touch -t 202401010800.30 file.txt

    This sets the timestamp of file.txt to January 1, 2024, 08:00:30 AM.

Update the timestamp using a human-readable date:

touch -d "2024-01-01 08:00:30" file.txt

Use a reference file to set the timestamp:

touch -r referencefile.txt file.txt

Create a file but do not create it if it doesn't exist:

touch -c nonexistingfile.txt


The touch command is mainly used to create empty files and update file timestamps (atime and mtime).
Key options include -a, -m, -c, -t, and -r, which allow you to control the timestamp behavior and prevent file creation if necessary.
It's commonly used in scripting, automation, and file management tasks to manage file metadata efficiently.
