# Create Backup

Insert SD card and find out which mounted disk maps to SD card
`diskutil list`

Create a backup

`sudo dd if=/dev/disk2 of=raspberrypi.dmg`

# Restore Backup

Insert SD card and find out which mounted disk maps to SD card
`diskutil list`

`diskutil unmountDisk /dev/disk5`

Format the disk using FAT16

`sudo newfs_msdos -F 16 /dev/disk5`

`sudo dd if=raspberrypi.dmg of=/dev/disk5`
