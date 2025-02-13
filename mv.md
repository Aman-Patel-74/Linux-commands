mv 
Basic Usage:

    Rename a file:

mv oldname.txt newname.txt

    This renames the file oldname.txt to newname.txt.

Move a file to a different directory:

mv file.txt /path/to/destination/

    This moves the file.txt to the specified directory (/path/to/destination/).

Move multiple files to a directory:

mv file1.txt file2.txt /path/to/destination/

    This moves both file1.txt and file2.txt to the specified directory.

Rename a directory:

mv olddir newdir

    This renames the directory olddir to newdir.

Move a directory to a different location:

    mv mydir /path/to/newlocation/

        This moves the entire directory mydir to the new location.

Commonly Used Options for mv:

    -i (interactive)
        Prompts for confirmation before overwriting an existing file. This helps prevent accidental data loss by ensuring you don't overwrite a file without realizing it.

mv -i sourcefile destinationfile

-f (force)

    Forces the move operation, even if it involves overwriting an existing file. It will not prompt you for confirmation.

mv -f sourcefile destinationfile

-u (update)

    Only moves the file if the source file is newer than the destination file or if the destination file is missing.

mv -u sourcefile destinationfile

-n (no-clobber)

    Prevents overwriting an existing file. If the destination file exists, it will not be replaced.

mv -n sourcefile destinationfile

-v (verbose)

    Provides a detailed output of the operation, showing what is being moved and where it is being moved.

mv -v sourcefile destinationfile

-b (backup)

    Creates a backup of the destination file before it is overwritten. You can specify the backup extension with the --suffix option.

mv -b sourcefile destinationfile

--backup

    Similar to -b, but allows you to specify which type of backup to make using --suffix or other backup options.

mv --backup=numbered sourcefile destinationfile

--help

    Displays help information for the mv command, including all available options and usage examples.

mv --help


The mv command is a versatile and essential tool in Linux for moving and renaming files and directories.
Commonly used options include -i for interactive mode, -f for forced moves, -v for verbose output, and -n for preventing overwrites.
By using these options, you can control how files are moved or renamed, whether you're overwriting existing files, creating backups, or simply renaming a file within the same directory.