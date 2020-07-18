# dd-assignment-3
1. Open 2 terminals, using cd &lt;folder_name&gt; to access the folder where the code is present
and other &#39;dmesg -wH&#39; to see the kernel log.
2. type &#39;make all&#39; to compile the program.
3. insert the kernal file using &#39;sudo insmod main.ko&#39;.

4. remove existing usb driver using &#39;sudo rmmod uas&#39; and &#39;sudo rmmod usb_storage&#39;.
5. Plug usb flash device and check if usb details is coming or not
6. type &#39;sudo fdisk -l&#39; to see if the usb_driver is seen or not... here it will show /dev/usb1.
Then proceed further.
7. create a folder in media directory using &#39;sudo mkdir /media/folder_name/&#39; Ex: sudo mkdir
/media/kusb/
8. type &#39;sudo mount -t vfat /dev/myusb1 /media/folder_name&#39; to mount the usb filesystem
into /media/foldername. Ex: sudo mount -t vfat /dev/myusb1 /media/kusb/
9. go to root directory by typing &#39;sudo -i&#39;
10. go to the directory where usb_driver is mounted. Ex: cd /media/kusb/
11. create a .txt file by typing &#39;echo &quot;write something&quot; &gt;text_file_name.txt&#39;.
12. With the help of command &#39;cat text_file_name.txt&#39;, you can see the content in the text file.
13. Leave from the media directory using &#39;cd ../..&#39; and unmount the file system using &#39;umount
/media/folder_name/&#39; Ex: umount /media/kusb/
14. to leave the root directory, type &#39;logout&#39;.
