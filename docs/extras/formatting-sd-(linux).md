---
title: Formatting SD (Linux)
---

# Formatting SD (Linux)
---

## Required Reading

This is an add-on section for formatting an SD card to work with the 3DS.

If the 3DS already recognizes the SD card, this guide is not required.

This page is for Linux users only. If you are not on Linux, check out the [Formatting SD (Windows)](formatting-sd-(windows).md) or [Formatting SD (Mac)](formatting-sd-(mac).md) pages.

## Instructions
### Section I - Determining which slot your SD card is in

1. Make sure your SD card is **not** inserted
1. Launch the Linux Terminal
1. Type `watch "lsblk"`
1. Insert your SD card into your PC
1. Observe the output. It should match something like this:
```
NAME        MAJ:MIN RM   SIZE RO TYPE MOUNTPOINT
mmcblk0     179:0    0   3,8G  0 disk
└─mmcblk0p1 179:1    0   3,7G  0 part /run/media/user/FFFF-FFFF
```
1. Take note of the device mount point. In our example above, it was `mmcblk0`
  + If `RO` is set to 1, make sure the lock switch is not slid down
1. Hit CTRL + C to exit the menu

### Section II - Formatting the card

![](https://upload.wikimedia.org/wikipedia/commons/8/85/Cfdisk_screenshot.png)

1. Type in `sudo cfdisk /dev/(device mount point from above)`
1. On each partition, hit `Delete`
1. Create a new Primary partition that covers the size of your entire SD card
	+ This will create a new partition with the linux filesystem
1. Select type and take a look at the menu
1. Find "W95 FAT32" and take note of the code on the left side of that text
1. Press any key, then enter the code you took note of in the previous step
1. Hit enter, then hit Quit
