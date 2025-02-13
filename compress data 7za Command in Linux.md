compress data 7za

7za Command in Linux 

The 7za command is a part of the 7-Zip software suite, which is a high-compression file archiver. The 7za command is the standalone version of 7-Zip, capable of creating and extracting 7z, tar, gzip, bzip2, and other archive formats.

The 7za tool is useful for compressing and decompressing files and directories efficiently, especially with the highly efficient 7z compression format.
Basic Syntax:

7za [options] [command] [archive_name] [file(s)]

    [options]: Flags that modify the behavior of the command.
    [command]: The operation to be performed (e.g., a for adding files, x for extracting).
    [archive_name]: The name of the archive (e.g., archive.7z).
    [file(s)]: The files or directories to be compressed or extracted.

Common Commands and Options for 7za:

    a – Add files to an archive
    The a command is used to create a new archive or add files to an existing archive.

7za a archive.7z file1.txt file2.txt

    This command creates (or updates) archive.7z and adds file1.txt and file2.txt to it.

x – Extract files from an archive
The x command is used to extract files from an archive.

7za x archive.7z

    This extracts all files from archive.7z into the current directory, preserving the directory structure.

e – Extract files to the current directory
The e command is used to extract files from an archive into the current directory, without preserving the directory structure.

7za e archive.7z

    This will extract all files from archive.7z into the current directory, without recreating the original folder structure.

l – List contents of an archive
The l command lists the contents of an archive without extracting it.

7za l archive.7z

    This will display the list of files contained in archive.7z.

t – Test the integrity of an archive
The t command is used to test the integrity of an archive.

7za t archive.7z

    This checks whether the archive.7z file is corrupted and validates its integrity.

d – Delete files from an archive
The d command allows you to delete files from an existing archive.

7za d archive.7z file1.txt

    This deletes file1.txt from archive.7z.

u – Update an existing archive
The u command is used to update an existing archive by adding or replacing files.

7za u archive.7z file2.txt

    This will update archive.7z by adding or replacing file2.txt.

-p – Set password for an archive
The -p option allows you to set a password for creating or extracting an encrypted archive.

7za a -pMyPassword archive.7z file1.txt

    This will create an encrypted archive archive.7z with the password MyPassword.

-m – Set compression method and options
The -m option allows you to specify the compression method and its options (e.g., dictionary size, compression level).

    7za a -m0=lzma archive.7z file1.txt

        This will use the LZMA compression method to compress file1.txt into archive.7z.

    -t – Specify the archive type
    The -t option allows you to specify the archive format (e.g., 7z, zip, tar, gzip).

7za a -tzip archive.zip file1.txt

    This command creates a .zip archive (instead of .7z) from file1.txt.

    -aoa – Overwrite all existing files without prompt
    The -aoa option forces the program to overwrite any existing files without prompting the user.

7za a -aoa archive.7z file1.txt

    This will overwrite any existing files in archive.7z without asking for confirmation.

    -mx – Set compression level
    You can adjust the compression level using -mx, where x is a value from 0 (fastest, least compression) to 9 (slowest, best compression).

7za a -mx=9 archive.7z file1.txt

    This compresses file1.txt with the highest compression level (9).

    -v – Split into volumes
    The -v option allows you to split the archive into volumes of a specified size.

7za a -v5m archive.7z file1.txt

    This creates multiple volumes of 5 MB each for the archive archive.7z.

Examples of 7za Command Usage:

    Create a 7z Archive from Files:

7za a archive.7z file1.txt file2.txt

    This creates archive.7z and compresses file1.txt and file2.txt into it.

Extract Files from a 7z Archive:

7za x archive.7z

    This extracts all files from archive.7z and restores their original directory structure.

List the Contents of a 7z Archive:

7za l archive.7z

    This lists the contents of archive.7z without extracting any files.

Test the Integrity of a 7z Archive:

7za t archive.7z

    This checks the integrity of archive.7z to ensure it is not corrupted.

Set a Password for an Archive:

7za a -pMySecretPassword archive.7z file1.txt

    This creates an encrypted archive.7z with the password MySecretPassword.

Update an Existing Archive:

7za u archive.7z file2.txt

    This updates archive.7z with the new or changed file2.txt.

Split an Archive into Multiple Volumes:

    7za a -v10m archive.7z file1.txt

        This splits archive.7z into 10 MB volumes while compressing file1.txt.

Help Commands for 7za:

    7za --help
    Displays a summary of the options and commands available with 7za.

7za --help

man 7za
Displays the manual page for 7za, detailing its usage, options, and examples.

man 7za

info 7za
Provides more detailed documentation, including advanced usage and options for 7za.

    info 7za

Conclusion:

The 7za command is a versatile file archiving and compression tool in Linux that supports a wide range of compression formats, including 7z, zip, tar, and gzip. It is particularly known for its high compression ratio, especially when using the 7z format.

Key operations include:

    a: Add files to an archive.
    x: Extract files from an archive.
    e: Extract files to the current directory.
    l: List archive contents.
    t: Test archive integrity.
    d: Delete files from an archive.
    u: Update an existing archive.