# Mt7922-sBluetooth-bugs-for-Linux-
if you install Linux Ubuntu for your computer, but you will find that Bluetooth can't be turned on, now you maybe try to find document and it useless 

if there are no issues your with your firmware and diver, youcan add support for mediatek MT7922 device(https://lkml. org/lkml/2024/3/15/325)

sudo apt-get update 
sudo apt-get install linux-soure #install the soure for linux. However, the default version might be the downloaded 5.15b version.

try wget http://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.8.tar.xz
and soure dome will be installed to /usr/src
cd /usr/src
tar -of linux-6.8.tar.xz #After decompression, a file will be generated.
cd linux-6.8
