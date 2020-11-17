# How to guide for setting up Ubuntu operating system
## Before you start <br>
Minimum specs: <br> 
1.00 GHz x86 processor (where x86 refers to the instruction set architecture of the CPU) <br>
1.00 GB of Random Access Memory (RAM) <br> 
8.60 GB of disk memory (the more the better) <br>
Video support of 1024 x 768 resolution <br>
If you are using an older machine, you may require the 32 bit version (see below) <br> 
## Download your disk image iso 
Get the newest version of Ubuntu 20.04 for 64 bit architecture at https://releases.ubuntu.com/20.04/ <br>
Or get an older version for 64 bit machine based on your specifications at http://old-releases.ubuntu.com/releases/ <br> 
Older machines that have 32 bit or i386 chips will require the alternate and/or older disk images. <br>
It helps to verify the md5 sum or sha256 sum of the iso file. This can ensure that it hasn't been altered or tampered with. <br>
To check the integrity of the iso, first get acces to `gpg` or `sha256` and test with `gpg --list-keys` <br> 
Then run `gpg --keyid-format long --verify SHA256SUMS.gpg SHA256SUMS` where the SHA256SUMS keys should come with Ubuntu or in CoreUtils for Linux. <br>     
If the output says you do not have the keys, you will to use the ID numbers from the keys and download them separately. <br> 
The command is as follows: `gpg --keyid-format long --keyserver hkp://keyserver.ubuntu.com --recv-keys key1 key2` <br>
A signed key means that it is nearly impossible mathematically that this file was tampered with, helping you ensure system security. <br>
Now check the iso by running: `sha256sum -c SHA256SUMS 2>&1 | grep OK` <br>
## Create a bootable USB drive or burn the iso image to a DVD  
Once you have the iso image, it should read like ubuntu-20.04.1-desktop-amd64.iso <br>
To make a bootable USB, the non-command line way requires you open Disks in Ubuntu. <br>
First, ensure that you have backed up any necessary or important data on this disk. <br>
Likewise, enure that it is formatted in the correct file system configuration. FAT systems allow cross OS compatibility between Mac, Linux, and Windows. <br>
Linux uses EXT4 and Windows uses NTFS <br> 
Select the appropriate file system and create a partition of a suitable size on your disk. <br>  
Then select your USB drive on the left side after inserting and mounting it, navigate to the 3 dots in the upper right corner, select Restore Disk Image, and choose the iso image that was just installed. <br> 
To restore a disk image from command line, use a low level utility like `dd` <br>
Other programs and methods exist to create partitions, initialize file systems, and restore disk images, such as for Mac and Windows users. <br> 
This process can take some time if you do a full re-format on a disk, as this goes through each bit and sets it back to zero. Consider just doing a simple re-format and use the old data as if it were empty memory. <br> 
Your bootable USB should be done in about 10 minutes. <br> 
For burning the image to a DVD, after inserting a blank disk, navigate to your downloaded ubuntu disk image, right click, and press Write To Disk. <br>
Make sure you select the correct image to write and the blank DVD to write onto, then press Burn. <br> 
You cold also use a utility such as Burner and follow similar steps. <br> 
## Prepare to install Ubuntu onto your machine!
  

  
