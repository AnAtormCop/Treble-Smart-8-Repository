# Fixing issues
  - Want to know how to fix issues? heres one of the super neat cool how!
  - also. YOUR RESPONSABLE FOR ANY DAMAGES
  - The Said / Report are made up!!

# System Size
  - User said. How to fix "Resizing 'system_a'                                FAILED (remote: 'Not enough space to resize partition')"?
  - This is fixable by doing this!
  - Reboot to fastboot first then type this command
    
    ``fastboot delete-logical-partition product_a``

    ``fastboot delete-logical-partition product_b``
    
    ``fastboot delete-logical-partition product``
    
    ``fastboot delete-logical-partition system_ext``
    
    ``fastboot delete-logical-partition system_ext_a``
    
    ``fastboot delete-logical-partition system_ext_b``
    
    ``fastboot -w ``

# Brightness Issue
  - User reported said : "Why is the screen so dim, how to fix it?"
  - Fix it by typing a single command! NO REBOOTS
  - Don't make the brightness larger "4065" pls
     ``setprop persist.sys.qcom-brightness 3900``
    
# Bricked
  - User said : "IM BOOTLOOPPINGGG AND CANT ACCESS TO TWRPPPP"
  >> Sybau.
  - In order to fix it. Download the spreadturm tool from releases then download the rom. extract the pac then do the spreadturm thing

# GSI Bootloop
  - User said : "IM BOOTLOOPING"
  - Reboot to recovery then format data. or reflash GSI

Thats all. 
