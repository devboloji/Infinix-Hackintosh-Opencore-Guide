
# Infinix-Hackintosh-Guide-Opencore
This repo contains the installation guide and EFI files required to get a perfectly functional and Big Sur and later Hackintosh on your Ice Lake (10th gen) Inbook or X1,slim. Everything is stable and functional as described in the Readme.
<hr>
These are the builts from me.  You might get the future updates for this machine.

 **I will try my best to keep the repo updated with the latest kexts and OpenCore version**
 -**For macOS Monterey this EFI will work great as BigSur, But bluetooth is not working Only in Monterey. Tried many ways to fix but may fix later releases. so don't expect flawless functionality**
Report me If you find the bugs or any issues. And don't ask for ETA.
- **With every EFI update you retrieve from here please remember to go through the post install guide**

![img](https://img.shields.io/badge/Release%20Update-July-red) ![img](https://img.shields.io/badge/macOS%20Support-Monterey--11.6.7-blue)![img](https://img.shields.io/badge/macOS%20Support-BigSur-blue) ![img](https://img.shields.io/badge/OpenCore%20Version-0.8.2-red)

# Introduction

EFI folder and Guide for Infinix X1,Slim and Infinix laptop Hackintosh Opencore.

- `Tested CPUs`: **i3-1005G1**(not tested in i5/i7, If anyone tested, Let me know: [facebook](https://www.facebook.com/sai.dev.92317) and [telegram](https://t.me/Pappusaidev))
- `Integrated Graphics`: **G1/G4 graphics**
- `Sound Card`: **ALC269 (use alcid=26)**
- `Wireless Cards Tested`: **Intel® Wi-Fi 6E AX210.**
<hr>


# What's Working.>>
- Wifi
- Bluetooth (Bluetooth Headphones working, also bluetooth file transfer works)
- App Store (see post install guide for more info)
- Onboard audio
- USB 2.0 / USB 3.0
- Wired headphones
- Trackpad
- brightness keys(To increase(+ve) -> `Pause`key) & (To decrease(-ve) -> `Scr Lk` key)
- OnBoard Audio Input and Output
- Wake / Shutdown
- Short sleep (.If you make sleep for long hours, The laptop shutdowns. To boot up your device you need to plug in the charge like macbook to wake. But you can make sleep to for 1 to 3 hours(but you will lose 2 to 3 percentage for every hour when  you put your device into sleep.) 
This is due to continuous fan spinning when sleep. Anyone is welcomed to fix these issues. First contact me to do that
- Everything (Much More).

## <What's Not working>
* Long Sleep(Using Long sleep, fans still spins and causes battery drain)(Use any hibernate app in macos) Any one is welcomed to fix this issue, contact me.
* Hdmi slot.

# Bios
- Note: Most of these options may not be present in your firmware, we recommend matching up as closely as possible but don't be too concerned if many of these options are not available in your BIOS
- ## Disable:
- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port(if you have)
- VT-d (can be enabled if you set DisableIoMapper to YES)
- CSM(you may not have in i3)
- Thunderbolt(For initial install, as Thunderbolt can cause issues if not setup correctly)
- Intel SGX
- Intel Platform Trust
- CFG Lock (MSR 0xE2 write protection)(This must be off, if you can't find the option then enable AppleXcpmCfgLock under Kernel -> Quirks. Your hack will not boot with CFG-Lock enabled)

- ## Enable:
- VT-x
- Above 4G decoding
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- DVMT Pre-Allocated(iGPU Memory): 256MB
- SATA Mode: AHCI
- Every setting is not Available so check your self
- Intel Virtualization Technology

# INSTALLATION
- ## macOS Big Sur Online Installer (Recomended)
This is a simple and quick summary of the online install USB creation

Windows Guide:
 - REQUIRED 4gb SDcard, Need to be format to fat32(MBR). Use any formatter to format.
 Note: Must format to MBR even you have UEFI System.

- 1.Download [rufus](https://rufus.ie/en/)
- 2.Select the desired flash drive you would like to put the installer on under the device option
- 3.Select> non-bootable <as the boot selection (REQUIRED)
- 4.Select> FAT-32 <or> Large FAT-32 <as the partition scheme
- 5.Open up the usb partition in file explorer and delete the files created by rufus
- 6.Create a folder on that partiton named> com.apple.recovery.boot <
- 7.Install [python](https://www.python.org/downloads/) (Make sure you select add python x.x to path)
- 8.Download and extract the [OpenCore Package](https://github.com/acidanthera/OpenCorePkg/releases)
- 9.Select the macrecovery folder in the opencorepkg folder at>  /Utilities/macrecovery/ <
- 10.Click on home > copy path at the top of file explorer
- 11.Fire up command prompt and type cd and hit spacebar and paste the path of the macrecovery folder.
- 12.Run the command:
 python macrecovery.py -b Mac-42FD25EABCABB274 -m 00000000000000000 download 
 - download starts.
- 13.This will put some files in the macrecovery folder but we only need <BaseSystem.dmg> and <BaseSystem.chunklist>
- 14.Paste both of those files in the> com.apple.recovery.boot < folder in your Sdcard or flash drive partiton
- 15.Download the latest EFI created [here](https://github.com/devboloji/Infinix_INBook_X1_XL11_i3-Hackintosh-Guide-Opencore/releases)
- 16.Copy the EFI folder and paste it in your USB partiton
Restart your laptop and go to bios and reboot from usb.
Note: Make sure to apply the correct bios settings before continuing (provided above)

# macOS Guide:
                                                                       
- 1.Launch Disk Utility
- 2.Select View > Show all devices at the top left
- 3.Select your flash drive and format it as MS-DOS (FAT) Use any formatter to format.
 Note: Must format to MBR even you have UEFI System.
- 4. Open up your usb partiton and create a folder named com.apple.recovery.boot
- 5.Download and extract the OpenCore Package
- 6.Select the macrecovery folder in the opencorepkg folder at /Utilities/macrecovery/
- 7.Right click and click "New terminal at folder"
- 8.Run the command:
 python macrecovery.py -b Mac-42FD25EABCABB274 -m 00000000000000000 download
- download in the terminal window
- 9.This will put some files in the macrecovery folder but we only need BaseSystem.dmg and BaseSystem.chunklist
- 10.Paste both of those files in the com.apple.recovery.boot folder in your flash drive partiton
- 11.Download the latest EFI created [here](https://github.com/devboloji/Infinix_INBook_X1_XL11_i3-Hackintosh-Guide-Opencore/releases)
- 12.Copy the EFI folder and paste it in your USB partiton
Note: Make sure to apply the correct bios settings before continuing (provided above)

Restart your laptop and go to bios and reboot from usb.

 # macOS BigSur Offline Installer from mac
- 1.Search and Download Olarila BigSur .raw from [Here](https://www.olarila.com/topic/6278-hackintosh-and-macintosh-olarila-vanilla-images-macos/)
- 2.Download etcher from [here](https://www.balena.io/etcher/)
- 3.Make Usb bootable (Flash the Sdcard) using Etcher and olarila bigsur.
- 4.mount the efi of Sdcard or bootable drive.
- 5.and paste the Efi to USB. Efi [here](https://github.com/devboloji/Infinix_INBook_X1_XL11_i3-Hackintosh-Guide-Opencore/releases)

Restart your laptop and go to bios and reboot from usb.
- 6. Boot to the usb.and install.Enjoy!!!!
Disclaimer - I am not Responsible for any cause of damage for your device.
- You can follow me on [facebook](https://www.facebook.com/sai.dev.92317) and [telegram](https://t.me/Pappusaidev)
                                                                       
Thanks to the OpenCore Team, SAITEJA for testing, also me ofcourse.

