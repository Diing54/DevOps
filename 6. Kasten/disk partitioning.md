
2025-02-16 17:15

Level : 

Tags :[[Linux]]

# disk partitioning

## Understanding Mounting
- In simple terms, we know mounting as inserting eg a usb drive into your computer 
- What really happens is that the system attaches a folder to the usb drive so that you can access its files. This happens to all other storage devices like a CD-ROM or a hard drive or even a floppy disk ( :) outdated) .The folder which the system attaches storage device is the mount point
- The main hard drive partition is mounted as "/" which is the root.
- CD-ROM - /media/cdrom
- USB drive - /mnt/usb
- NOTE - Suppose i wish to mount the CD-ROM which is located at /dev/sr0 to the mount point or folder /media/cdrom I need to be careful and understand that the files and subdirectories on CD-ROM will fall under /media/cdrom and any files that were originally at /media/cdrom will not be visible although they are present. When i unmount the CD-ROM the original files at /media/cdrom will become visible again.
- sudo mount /dev/sr0 /media/cdrom  - command for mounting
## Partitions
- A partition is like a section or part of a hard drive. Analogy, a house being the hard drive and rooms being partitions where each partition stores different stuff in it.
- In linux, hard drives are located in the /dev/ folder and are named as follows:
1. /dev/sda - first drive
2. /dev/sdb - second drive
3. /dev/sdc - third drive
- Then partitions are labelled with numbers as follows:
1. /dev/sda1 - first partion on the first drive
2. /dev/sda2 - second partition on the first drive
- In the past, different types of hard drives had different names but this changed because of hotplug which is a new feature which unifies device management
- lsblk - command for listing all the drives and partitions
- df -h - command for viewing disk usage



## References
