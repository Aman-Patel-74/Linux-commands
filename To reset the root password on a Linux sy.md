To reset the root password on a Linux system, follow these steps:

# Steps to Reset Root Password

1. Reboot the System:
   Restart your computer and access the boot menu. This is usually done by pressing a key such as `Esc`, `F2`, `F12`, or `Del` during the boot process.

2. Access GRUB Menu:
   If you are using a GRUB bootloader, you will see the GRUB menu. Select the boot entry you want to modify and press `e` to edit it.

3. Edit GRUB Entry:
   Find the line that starts with `linux` or `linux16`. At the end of this line, add `init=/bin/bash`.

4. Boot with Modified Entry:
   Press `Ctrl + X` or `F10` to boot with the modified entry. This will boot you into a root shell.

5. Remount Filesystem:
   Remount the filesystem as read-write:
  
   mount -o remount,rw /
 

6. Change Root Password:
   Use the `passwd` command to change the root password:
  
   passwd
 

7. Reboot the System:
   After changing the password, remount the filesystem as read-only and reboot:
  
   mount -o remount,ro /
   exec /sbin/init
 

# Example Commands


# Remount filesystem as read-write
mount -o remount,rw /

# Change root password
passwd

# Remount filesystem as read-only and reboot
mount -o remount,ro /
exec /sbin/init


This process will reset the root password. Make sure to remember the new password for future use.