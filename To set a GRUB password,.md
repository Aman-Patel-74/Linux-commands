To set a GRUB password, follow these steps:

# Steps to Set a GRUB Password

1. Generate a Password Hash:
   Use the `grub-mkpasswd-pbkdf2` command to generate a hashed password.
 
   grub-mkpasswd-pbkdf2

   Enter your desired password when prompted. The command will output a hashed password.

2. Edit the GRUB Configuration File:
   Open the `/etc/grub.d/40_custom` file with a text editor using `sudo`.
 
   sudo nano /etc/grub.d/40_custom


3. Add the Password Entry:
   Add the following lines to the file, replacing `your_hashed_password` with the hashed password generated in step 1.
plaintext
   set superusers="root"
   password_pbkdf2 root your_hashed_password


4. Update GRUB Configuration:
   Update the GRUB configuration to apply the changes.
 
   sudo update-grub


# Example

1. Generate Password Hash:
 
   grub-mkpasswd-pbkdf2

   Output:
plaintext
   Enter password: 
   Reenter password: 
