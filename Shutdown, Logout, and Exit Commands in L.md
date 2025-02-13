Shutdown, Logout, and Exit Commands in Linux

In Linux, there are several commands used to shutdown, log out, and exit from the system or from a session. These commands are crucial for system maintenance, user management, and process termination. Below is a detailed explanation of the commands related to shutting down, logging out, and exiting in Linux.
1. shutdown Command in Linux

The shutdown command is used to shut down or reboot the system in a safe manner. It allows you to halt all processes, close files, and shut down the system properly.
Basic Syntax of the shutdown Command:

shutdown [OPTION] [TIME] [MESSAGE]

    OPTION: Specifies the operation to be performed (e.g., shutdown, reboot, etc.).
    TIME: Specifies when to perform the shutdown (can be a specific time or relative time).
    MESSAGE: An optional message to notify users about the shutdown.

Examples of Using the shutdown Command:

    Shutdown the system immediately:

sudo shutdown now

    This shuts down the system immediately.

Shutdown the system after a specific time:

sudo shutdown 10

    This shuts down the system after 10 minutes.

Shutdown the system at a specific time:

sudo shutdown 22:00

    This shuts down the system at 10:00 PM.

Shutdown the system with a custom message:

sudo shutdown +5 "System will shut down in 5 minutes"

    This shuts down the system in 5 minutes and sends a custom message to all users.

Cancel a scheduled shutdown:

sudo shutdown -c

    This cancels any previously scheduled shutdown.

Reboot the system:

sudo shutdown -r now

    This reboots the system immediately.

Shutdown with a time delay (e.g., 30 minutes):

    sudo shutdown +30

        This will shut down the system after 30 minutes.

Help for shutdown Command:

You can get more details about the shutdown command using:

man shutdown

or

shutdown --help

This will display the manual page or the help section for the shutdown command.
2. logout Command in Linux

The logout command is used to log out from the current shell or session. This command is most commonly used in terminal sessions, whether you are working on a local machine or through SSH.
Basic Syntax of the logout Command:

logout

    The logout command does not take any arguments or options. It simply logs you out of the current session.

When to Use logout:

    Terminal or Console Session: When you are logged into a terminal or console session and want to end your session, you use the logout command.

    Remote Session (SSH): If you are logged into a remote machine via SSH, the logout command ends the remote session and returns you to your local shell.

Examples of Using the logout Command:

    Log out of the current shell:

logout

    This logs out the current session.

Log out from an SSH session:

    logout

        This logs you out of the SSH session and disconnects from the remote machine.

Help for logout Command:

The logout command does not have a detailed man page, but you can get basic help using:

help logout

3. exit Command in Linux

The exit command is used to exit from the current shell session or script. It's similar to logout but more commonly used to exit from scripts or terminal shells.
Basic Syntax of the exit Command:

exit [n]

    n: An optional argument where you can provide an exit status code. By convention, an exit status of 0 indicates success, and any non-zero value indicates an error.

Examples of Using the exit Command:

    Exit the current shell with a default exit code (0):

exit

    This exits the current terminal session and returns control to the parent process (e.g., the terminal window or SSH session).

Exit a shell with a specific exit code:

exit 1

    This exits the shell and returns an exit status code of 1, which typically indicates an error or abnormal termination.

Exit from a script:

In a script:
exit 0

    This command can be used inside a shell script to exit the script. It is common to use exit 0 to indicate successful completion of the script.

Exit from an SSH session:

exit

    This logs out and closes the SSH connection.

Exit from a nested shell:

    exit 0

        If you have launched a subshell (for example, using bash or sh), using the exit command will close that subshell and return to the parent shell.

Help for exit Command:

The exit command is built into the shell, and you can get basic help with:

help exit

For more details on exit status codes:

man bash

Look for the Exit Status section in the manual.
Summary of Key Commands:

    shutdown: Used to shut down or reboot the system. It can schedule a shutdown and display custom messages.
        Example: sudo shutdown -r now (Reboot now).
        Example: sudo shutdown +10 (Shutdown in 10 minutes).

    logout: Used to log out of the current shell or session.
        Example: logout (Exit the current shell session).

    exit: Used to exit the current shell or terminal session. It can also be used in scripts to indicate successful or unsuccessful execution.
        Example: exit 0 (Exit with success status).

When to Use Each Command:

    shutdown: When you want to shut down or reboot the system completely.
    logout: When you are done with a terminal or console session and want to log out of the current session.
    exit: When you are finished with a shell session, or a script has completed, and you want to exit with a specific exit status.

Conclusion:

Understanding the usage of shutdown, logout, and exit commands is vital for effectively managing your Linux sessions and systems. Each command serves a different purpose: 
