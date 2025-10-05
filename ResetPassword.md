### Reboot the System
Reboot the system using:

- sudo reboot

### Access the GRUB Menu
During the boot process, hold Shift (for BIOS systems) or press Esc repeatedly (for UEFI systems) to access the GRUB menu.

### Edit GRUB Menu
Highlight the default boot entry (usually the first one).
Press e to edit the selected GRUB entry.

### Modify Kernel Parameters
Locate the line that starts with:

linux /boot/vmlinuz-<version> ...

Replace ro with rw and append init=/bin/bash at the end of the line. The modified line should look similar to:
javascript

linux /boot/vmlinuz-<version> root=/dev/sda1 rw init=/bin/bash

### Boot into Rescue Mode
Press Ctrl+X or F10 to boot with the modified parameters. This will start the system in single-user mode with a root shell.

### Remount the Filesystem
Remount the root filesystem as read-write:

- mount -o remount,rw /

### Reset the Root Password
Change the root password by running:

- passwd
Enter the new password when prompted.

### Update SELinux Context (if applicable)
If SELinux is enabled on your system, you must relabel the filesystem to apply the new password. Run:

- touch /.autorelabel

### Reboot the System
Remount the root filesystem as read-only:

- mount -o remount,ro /

Reboot the system:

- exec /sbin/init
