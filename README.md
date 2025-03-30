# Mt7922-sBluetooth-bugs-for-Linux-
#if you install Linux Ubuntu for your computer, but you will find that Bluetooth can't be turned on, now you maybe try to find document and it useless 
#if there are no issues your with your firmware and diver, youcan add support for mediatek MT7922 device(https://lkml. org/lkml/2024/3/15/325)

sudo apt-get update 
sudo apt-get install linux-soure #install the soure for linux. However, the default version might be the downloaded 5.15b version.

try wget http://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.8.tar.xz
and soure dome will be installed to /usr/src
cd /usr/src
tar -of linux-6.8.tar.xz #After decompression, a file will be generated.
cd linux-6.8

save https://lkml. org/lkml/2024/3/15/325 and rename to bluetooth.patch
The specific operation of this step is wget -0 bluetooth.patch "https://lkml. org/lkml/2024/3/15/325"

sudo patch-p1 </path/to/bluetooth.patch  #Apply the patch to the source code that has been decompressed.
grep-A5 "13d3.*3585" drivers/bluetooth/busb.c #check it 

#Compiling and Installing the Kernel
Install the necessary build tools and dependencies：sudo apt-get install build-essential fakeroot dpkg-dev flex bison libssl-dev
sudo vim Makefile
now you can see EXTRAVERSION and NAME. first of them is your kernel's name and it must start with "-",like:-name-vi

#Configure, compile and install the kernel.
sudo make oldconfig
sudo make
sudo make modules_install
sudo make install
sudo update-grub
sudo reboot

now, you can enjoy your bluebooth





