# Step by Step 
First of all I made the 2 partitions on my usb stick drive , ext3 & ext4 partition . 
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/File-System-Stack-Task/gparted.png)

---
Now we need to make sure to auto mount the partitions whenever we insert the usb drive. So , In order to acheive this we need to make a directory to be the mounting point.
I will make 2 directories (ext3_dir , ext4_dir) 
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/File-System-Stack-Task/mounting_directories.png)

After that I will use gnome-disks in order to generate the format to auto mount & choose the mounting point for the partitions ( also I can write it manually the format is easy to understand ) 
Also , I didn't use the partition path from `/dev` path. I used `$ blkid` command  in order to get `UUID` so it connects to the device node directly. 

#### Making directories 
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/File-System-Stack-Task/mounting_directories.png)

#### UUID
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/File-System-Stack-Task/blkid.png)

#### Gnome-Disks 
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/File-System-Stack-Task/gnome-disks.png)

#### /etc/fstab 
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/File-System-Stack-Task/fstab.png)

#### After restarting my machine 
![](https://github.com/MonerMo/Embedded-Linux-Diploma-Tasks-Solution/blob/File-System-Stack-Task/ext3%2Cext4.png)

