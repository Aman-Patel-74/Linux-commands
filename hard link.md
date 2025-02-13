Create a hard link: Ln


ln sourcefile linkfile


    This creates a hard link named linkfile that points to sourcefile.

Create a symbolic link:

ln -s /path/to/original /path/to/symlink

    This creates a symbolic link named symlink pointing to original.

Create a symbolic link with a relative path:

ln -sr /path/to/original /path/to/symlink

    Creates a symbolic link with a relative path.

Force the creation of a link, even if the destination exists:

ln -f sourcefile symlink

Create a symbolic link interactively:

ln -si sourcefile symlink

The ln command in Linux creates links between files or directories.

Hard links point directly to the data blocks of a file, whereas symbolic (soft) links reference the file's path.
By using options like -s, -f, and -v, you can control how links are created and manage existing files more efficiently.
