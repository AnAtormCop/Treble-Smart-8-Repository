 <img src="https://raw.githubusercontent.com/AnAtormCop/Treble-Smart-8-Repository/refs/heads/main/Images/Picsart_26-01-20_00-23-25-437.png" width="100%" alt="Banner">

> [!WARNING]
>
> You are Accessing this Guide for the ones who dont have a PC and have a OTG & Rooted Device. But no worries, it will help you!
> 

  # Spreadturm Termux 
   Its ported, its basically linux edition, nothing special.
  # Requirements 
  • Rooted Device

  • Termux on Github / F-Droid

  • Infinix Phone

  • Type SU to grant superuser permissions, DONT EXIT
 
  # Making Directory called = chrootubuntu to /data/local/tmp/
    mkdir /data/local/tmp/chrootubuntu
    cd /data/local/tmp/chrootubuntu
   # Get Ubuntu 22 rootfs (required)
    busybox wget https://cdimage.ubuntu.com/ubuntu-base/releases/22.04/release/ubuntu-base-22.04-base-arm64.tar.gz
   # Extract the file and create needed directories 
     tar xvf ubuntu-base-22.04-base-arm64.tar.gz
     mkdir dev/shm
     mkdir sdcard
     cd ../
   # Create the script called start.sh and add this script (Research "vi" to avoid confusions) 
     vi start.sh  
   # Paste this
     #!/bin/sh
     #Create mkdir
     mkdir /dev/shm
     #The path of ubuntu rootfs
     UBUNTUPATH="/data/local/tmp/chrootubuntu"

    #Make needed files AGAIN
    mkdir $UBUNTUPATH/sdcard
    mkdir $UBUNTUPATH/dev/shm

    #Fix setuid issue
    busybox mount -o remount,dev,suid /data

    busybox mount --bind /dev $UBUNTUPATH/dev
    busybox mount --bind /sys $UBUNTUPATH/sys
    busybox mount --bind /proc $UBUNTUPATH/proc
    busybox mount -t devpts devpts $UBUNTUPATH/dev/pts

    #/dev/shm for Electron apps
    busybox mount -t tmpfs -o size=256M tmpfs $UBUNTUPATH/dev/shm

    #Mount sdcard
    busybox mount --bind /sdcard $UBUNTUPATH/sdcard

    #chroot into Ubuntu
    busybox chroot $UBUNTUPATH /bin/su - root

  # Exit vi and execute the file
   Press ESC then type :qw
   After that, start pasting this command
   
    chmod +x start.sh
    ./start.sh  
  # Paste this last command, don't exit
    echo "nameserver 8.8.8.8" > /etc/resolv.conf
    echo "127.0.0.1 localhost" > /etc/hosts

    groupadd -g 3003 aid_inet
    groupadd -g 3004 aid_net_raw
    groupadd -g 1003 aid_graphics
    usermod -g 3003 -G 3003,3004 -a _apt
    usermod -G 3003 -a root

    apt update
    apt upgrade

    apt install nano vim net-tools sudo git
 <div align="Left">
  <img src="https://raw.githubusercontent.com/AnAtormCop/Treble-Smart-8-Repository/refs/heads/main/Images/Picsart_26-01-19_23-22-00-909.png" width="100%" alt="Gud">

  # After you did the chroot tutorial, lets move to this guide
   Requirements
    • Make sure your on Localhost
    • Sudo apt-get works
    • DON'T EXIT
  # Double check if updated
    apt update && apt upgrade -y 
  # After that, Install drivers
    sudo apt-get install build-essential libusb-1.0-0-dev git wget curl unzip zip
    curl -L -O https://github.com/Seuj09/Spd_dump_termux/releases/download/Release/spreadtrum_flash_termux.zip
    unzip spreadtrum_flash_termux.zip
    cd spreadtrum_flash_termux
    chmod +x spd_dump
    chmod +x menu.sh
    chmod +x gen_spl-unlock
    chmod +x gen_spl-unlock-legacy
    chmod +x gen_fdl1-dl
    chmod +x misc-fastbootd.bin
    chmod +x misc-wipe.bin

  # Results
   Type ./menu.sh to start 

  # Credits
   @Seuj09 = Tutorial 
   
   @AnAtormCop = Repository 
   
   @Massatrio = Tools
