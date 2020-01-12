Odroid_C2_multiboot_scripts
==========

*Collection of scripts for usage on the Odroid C2 when using multiboot.*  

1. About
--------

These scripts contain small parts which are specific to my setup so you have to check the scripts and edit them to fit your own system setup.  
Three folders right now: 
- **boot.ini** confirmed working boot.ini files for various OS'. Edit accordingly to your own setup!
- **boot_scripts** scripts to directly boot into the chosen OS. Requirements: multiboot partition has to be mounted RW for this to work. **WARNING:** scripts contain relative paths to get it working universally in all OS', scripts will break when moved 
- **ubuntu_etc-kernel-postinst.d** script to run after an ubuntu kernel update, It copies the respective files to the multiboot location and makes a backup of the old files. File has to be placed in /etc/kernel/postinst.d
- **ubuntu_etc-initramfs-tools-hooks** script to run after update-initramfs, It makes a backup of the old multiboot uInitrd, it generates an uInitrd from the current initrd.img and copies it to the multiboot directory.
