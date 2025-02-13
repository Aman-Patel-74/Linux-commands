Commonly Used Options for uname:

    -s (kernel name)
        Displays the name of the kernel.

uname -s

    Example output:

    Linux

-n (network node name)

    Displays the network node hostname (the system name).

uname -n

    Example output:

    myhostname

-r (kernel release)

    Displays the version of the kernel.

uname -r

    Example output:

    5.4.0-42-generic

-v (kernel version)

    Displays the version of the kernel, including additional details like the build date.

uname -v

    Example output:

    #46-Ubuntu SMP Thu Jun 4 15:39:10 UTC 2020

-m (machine hardware name)

    Displays the machine architecture (e.g., x86_64 for 64-bit architecture).

uname -m

    Example output:

    x86_64

-p (processor type)

    Displays the type of processor.

uname -p

    Example output:

    x86_64

-i (hardware platform)

    Displays the hardware platform (e.g., x86_64 for a 64-bit Intel/AMD platform).

uname -i

    Example output:

    x86_64

-o (operating system)

    Displays the operating system name.

uname -o

    Example output:

    GNU/Linux

-a (all information)

    Displays all available system information, including kernel name, node name, kernel release, kernel version, machine hardware, processor type, hardware platform, and operating system.

uname -a

    Example output:

    Linux myhostname 5.4.0-42-generic #46-Ubuntu SMP Thu Jun 4 15:39:10 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux

--help

    Displays a help message with available options and their usage.

uname --help

--version

    Displays the version information of the uname command.

    uname --version

Examples of uname Command Usage:

    Display the kernel name:

uname -s

    Example output:

    Linux

Display the system's hostname:

uname -n

    Example output:

    myhostname

Display the kernel version:

uname -r

    Example output:

    5.4.0-42-generic

Display all system information:

uname -a

    Example output:

    Linux myhostname 5.4.0-42-generic #46-Ubuntu SMP Thu Jun 4 15:39:10 UTC 2020 x86_64 x86_64 x86_64 GNU/Linux

Display the machine hardware name:

uname -m

    Example output:

    x86_64

Display the operating system:

uname -o

    Example output:

        GNU/Linux

Additional Help Options:

    --help
        Displays a summary of available options and their descriptions for the uname command.

uname --help

man uname

    Displays the manual page for uname, providing a detailed explanation of the command and all of its options.

    man uname

Conclusion:

    The uname command is a simple but useful tool for displaying system information in Linux.
    It provides details about the kernel name, version, machine architecture, hostname, and more, which can help in troubleshooting, system configuration, or when checking the system's environment.
    The command has several options that allow you to tailor the information displayed, such as -a for all details or -s for the kernel name.
    Use man uname for more detailed documentation on the command.

