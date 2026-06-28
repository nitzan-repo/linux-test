linux-test
Today is a very big day for your Linux team. Today you are about to show all of the department the Linux environment you have created and developed way long ago when you were a DevOps course student.
Unfortunately, there was a mistake… Read the email you have got from your manager and start working!

Hello,
As you know, today was supposed to be your presentation day, when you had to show us what you have done in your DevOps course.
Unfortunately, everything was deleted.
The show must go on, you still need to show us the outcome.
These are the things that you need to create all over again:
●	Create a new Linux server named ServerLXF01. The server should be Ubuntu 22 and have the default configuration. The server should use a free-tier instance type.
●	Once your server is up and running, make sure you can connect to it and continue to the following steps.
●	Create a new directory called My_files (Make sure its have been created) and create two files in it (file 1, 2) by using one command.
 These files need to have execution permissions, for users(Use one command only)
Mkdir My_Files
touch file{1..2}
chmod 001 file1 file2


●	In your AWS machine, Create a new volume (gp3, 5GB), its name will be /dev/sdf.
Check your new disk. Check your free space in your disk


 
Lsblk
Df -h

●	Create two partitions from the disk. Each partition contains 500 MB. Make sure these partitions were created
sudo fdisk /dev/nvme1n1


 
●	Inform the OS that you have created new partitions and create xfs filesystem on the the first partition you have just created
  sudo partprobe /dev/nvme1n1
      sudo mkfs.xfs /dev/nvme1n1p1
	sudo mkfs.ext4 /dev/nvme1n1p2


●	Create a new folder named directory and check for mountpoint
mkdir directory
findmnt /directory
 
●	Find the uuid of the partition and add the mount point to the suitable file.
sudo mount /dev/nvme1n1p1 /directory
sudo blkid /dev/nvme1n1p1
sudo vim /etc/fstab
sudo umount /directory
sudo mount -a

Please hurry up, the Head of the department is coming to see their outcomes in a couple of hours.

thank you,
Jacki
Head of Linux Team



Good luck on your mission




