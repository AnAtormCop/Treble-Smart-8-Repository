# Infinix Smart 8 [Treble] Repository
  - There will be a list of GSI which you can visit on [Releases](https://github.com/AnAtormCop/Treble-Smart-8-Repository/releases)
  - Report Bugs on [Issues](https://github.com/AnAtormCop/Treble-Smart-8-Repository/issues)
# Requirements
  - Must have Infinix Smart 8 HD
  - [OPTIONAL] Must have a SD Card (to store gsi images)
  - System Partition Size [NOT THE IMAGE] for ur phone must be at minimium : 1gb and the Maxinum : 3.54gb
  - ADB And Fastboot Drivers. Get it from this [Repository](https://github.com/fawazahmed0/Latest-adb-fastboot-installer-for-windows) [ty fawazahmed0 💙]
  - Android 13 GSI ofc
# Installation
  - In order to flash GSI, there are TWO Methods of doing so, TWRP or Fastboot
  - Must have the TWRP File so. goodluck with that 😆
  - Your responsable for any modification to the phone. Any excuses to the tutorial will not be replied to ANYTHING else
# TWRP Method
  - Must have a vendor_boot.img by massatrio
  - 🧠
  - Extracted GSI File
  INSTALLATION [Fastboot Required]
  1. Reboot to bootloader then type fastboot flash vendor_boot_a [File]
    - If you are in slot A or B. change the a to ur slot. Check fastboot getvar all to check ur slot
  2. Download the file from Releases then after that. Select it and drag it to the cmd. Or type the directory, Exammple : "C:\Files\vendor_boot_a.img"
  3. Click enter then wait it to finish and ur done. then reboot to recovery

  now here we are.. GSI INSTALLATION
  1. Click Install
  2. Go to the file where you downlaoded
  3. If you see nothing. click install image then click the GSI IMG then select the option "System Image A" then swipe the bar then wait it to finish
  4. Then Format Data ofc then reboot
# Fastboot Method
  - Just extracted GSI File
  - PC ONLY. or your otg device
  - Flash TWRP From massatrio
    
  INSTALLATION
  1. Reboot ur phone to Fastboot
  2. Type Fastboot -w then type fastboot flash system_a [File]
  3. Download the GSI from Releases then after that. Select it and drag it to the cmd. Or type the directory, Exammple : "Fastboot flash system_a C:\Files\ahhgsilowthanurmom.img"
       - System Partition Size [NOT THE IMAGE] for ur phone must be at minimium : 1gb and the Maxinum : 3.54gb
  4. Click enter then wait to finish
  5. Reboot

# Question And Answers
  Q: Why does it says "Resizing 'system_a'                                FAILED (remote: 'Not enough space to resize partition')" when i flash the gsi?
  
  A: This shows that theres **NO** enough space for system partition. You can visit fixes on here :

  Q: Why does Infinix GSI Causes brightness bugs
  
  A: Honestly, Ask the group. I dont know why..

  Q: Do you have por-
  
  A: No. now sybau

  Q: Does System Size changes by installing Stock Rom?
  
  A: Obviously yea. Because it adds back the parttitions you removed

  Q: Do you have discord
  
  A: Probably Soon

  Q: Type an new lua
  
  A: ``print("hey")``

Any Infomation you want to know must be on issues!

# Extras 
"Just be happy if it boots. If more than just booting works, feel extremely lucky" - TrebleDroid
  - For help. Contact our search "Infinix Smart 8" on telegram
  - Also Join TS8 Group where we share modules or anything!
# Credits
  - Github Repo : Windows11
  - TWRP File : Massatrio
  - TrebleDroid Repo : TrebleDroid
  - GSI : Every GSI Maker to make this repo possible 💙 we support ur progress

