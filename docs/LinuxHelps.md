

Linux File System Notes

Root: - it can mean 3 different things
There is a Root User
a Root of the file system
folder named root (home folder for the root user)

We can hide files and directories by putting a dot “.” in front of it

We can toggle viewing hidden items by:  Ctrl+H

useful commands:
touch - create file(s)  (separate filenames with a space)
nano - edit file
cat - view file
pwd - view current path

to go to the Home directory:
$ cd ~   (tilde)

Directories of interest (not a full list):
proc - directory with PID (process id) as fhe sub directory names.  usefule for developers.  contains all data regarding a running process
opt - optional software located here
media - OS mounted media
mnt - manually mounted media 
bin - binaries.  programs used by OS here
boot - system level - no access.  boot files needed by the kernel
cdrom - legacy folder
dev - devices (e.g. keyboard, mouse, etc drivers)
etc - configuration files.  pronounced ‘etcetera’ by many.  Dennis Richie (co-founder of linux) said so
home - all user files.  also where terminal opens by default
usr - universal system resources.  icons as an example.  user app installs
tmp - temporary directory.  goes away when rebooted.  used by running apps.



