# Bootable Win10 on USB... Created on Linux!
This is a guide on how to create a bootable USB stick of Windows 10 on Linux

## Resources
https://itsfoss.com/bootable-windows-usb-linux/
Note: The steps in this link don't really work as advertised... So I made this.

## Step 1: Install woe
```
sudo add-apt-repository ppa:nilarimogard/webupd8
sudo apt update
sudo apt install woeusb
```

## Step 2: Format USB Drive
You have to make sure the drive is not in use. It can be very finiky in this way. I was having issue with it, so I just yanked the drive out and plugged it back in :-)

This all assumes the drive is at /dev/sdg

`sudo wipefs --all /dev/sdg`

## Step 3: Download Windows 10
I downloaded the ISO from: 
https://www.microsoft.com/en-us/software-download/windows10ISO
...It's about 5GB

## Step 4: Create bootable drive
`sudo woeusb --target-filesystem NTFS --device ~/Downloads/Win10_1809Oct_v2_English_x64.iso /dev/sdg`

# ... And you're done!
