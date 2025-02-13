rm file.txt

    This deletes the file file.txt. The file is permanently removed and cannot be recovered unless you have backups or are using a file system with snapshots.

Delete multiple files:

rm file1.txt file2.txt file3.txt

    This deletes all the listed files (file1.txt, file2.txt, file3.txt).

Delete all files in a directory:

    rm *.txt

        This deletes all files in the current directory that match the pattern *.txt.

Commonly Used Options for rm:

    -i (interactive)
        Prompts for confirmation before deleting each file. This helps prevent accidental deletions.

rm -i file.txt

-f (force)

    Forces the removal of files without prompting for confirmation. It will also remove read-only files without asking.

rm -f file.txt

-r or -R (recursive)

    Deletes directories and their contents recursively. This is useful when you need to delete a directory and all files within it.

rm -r mydir

-v (verbose)

    Provides detailed output, showing which files are being deleted.

rm -v file.txt

-d (directory)

    Removes empty directories. If you want to delete an empty directory, this option can be used with rm (without using -r).

rm -d emptydir

--no-preserve-root

    By default, rm refuses to remove the root directory (/). This option overrides that behavior (used cautiously).

rm --no-preserve-root -rf /

--help

    Displays help information for the rm command, listing all available options and their usage.

rm --help

--

    Marks the end of options, useful if the file names start with a hyphen (e.g., -file.txt).

rm -- -file.txt
Option	Description
-p, --parents	Creates parent directories as needed.
-m, --mode=MODE	Sets the permissions of the new directories.
-v, --verbose	Prints a message for each directory created.
--help	Displays help information about the command.
--version	Displays version information for the command.

rm 
Option	Description
-r	Recursively removes directories and their contents.
-f	Forces removal without prompting for confirmation.
-i	Prompts before every removal.
-v	Displays what is being done, showing which files are removed.
--help	Displays help information about rm command.
--version	Shows version information for the rm command.

rmdir: Can only delete empty directories. It is safer in the sense that it will not delete the contents of a directory, unlike rm -r.