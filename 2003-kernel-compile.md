# kernel compile

#show all
uname -a
#show kernel version
uname -r
cd /boot
    vmlinuz...
    initramfs...
cd /usr/src
download kernel
    kernel.org
    http ===>> click here
        linux
            kernel
                download version kernel
wget (link version kernel .tar.xz)
tar -jxvf linux.tar.xz
#we make link because you have so many kernel linux
ln -s linux-4.14.3 linux
cd /linux
    Documentation ===>> all information about kernel version
    README ===>> more information
yum groupinstall "Devlopment tools"
yum install Devlopment tools elfutils-libelf-devel openssl-devel ncures-devel qt-devel

#make 
#show switch
make help

#config kernel 
make config

#sow menue
make nconfig

#sow menue
make xconfig

#make to fresh
make clear

#remive all generates
mrproper

#ask everything
config

########################################
#recomend
#save and exit
menuconfig

#see .config
ls -a

#make file
make bzImage

#kernel is here
#you shouldn't change directory
#pwd
/usr/src/linux

#install modules
make modules

#where is modules in linux
ls /lib/modules

#install modules
make modules_install

#copy file in /boot
make install

#see new version of linux kernel
ls /boot

#reboot server
reboot
#you can see your new kernel in bootloader


#permanent

#command
grub2-set-default 'CentOS Linux (4.14.3) 7 (Core)'
grub2-reboot 'CentOS Linux (4.14.3) 7 (Core)'




#########################################
#show list modules
lsmod
rmmod
insmod
#remove modules
modprobe -r NAME_MODULES

#enable modules
modprobe NAME_MODULES

#information about modules
modinfo NAME_MODULES

#permanent
#can load and unload kerner modules permanent
cd /etc/sysctl.conf

#read file again
sysctl -p

#change file with out open it
sysctl -w net.ipv4.ip_forward=1
#######################################

 






