
# Infinix-Hackintosh-Guide-Opencore
This repo contains the installation guide and EFI files required to get a perfectly functional and Big Sur and later Hackintosh on your Ice Lake (10th gen) Inbook or X1,slim. Everything is stable and functional as described in the Readme.
<hr>
These are the builts from me.  You might get the future updates for this machine.

 **I will try my best to keep the repo updated with the latest kexts and OpenCore version**
 -**For macOS Monterey this EFI will work great as BigSur, But bluetooth is not working Only in Monterey. Tried many ways to fix but may fix later releases. so don't expect flawless functionality**
Report me If you find the bugs or any issues. And don't ask for ETA(Estimated Time of Time).
- **With every EFI update you retrieve from here please remember to go through the post install guide**

![img](https://img.shields.io/badge/Release%20Update-July-red) ![img](https://img.shields.io/badge/macOS%20Support-Monterey--11.6.7-blue)![img](https://img.shields.io/badge/macOS%20Support-BigSur-blue) ![img](https://img.shields.io/badge/OpenCore%20Version-0.8.2-red)

# Introduction

EFI folder and Guide for Infinix X1,Slim and Infinix laptop Hackintosh Opencore.

- `Tested CPUs`: **i3-1005G1**(not tested in i5/i7, If anyone tested, Let me know: [facebook](https://www.facebook.com/sai.dev.92317) and [telegram](https://t.me/Pappusaidev))
- `Integrated Graphics`: **G1/G4 graphics**
- `Sound Card`: **ALC269 (use alcid=26)**
- `Wireless Cards Tested`: **Intel® Wi-Fi 6E AX210.**
<hr>


# What's Working.
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

## What's Not working
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

### Note: If you need to edit Config.plist, don't Clover configurator because its opencore. Use OpenCore configurator , use PlistEdit pro, PropperTree, or Xcode.

# INSTALLATION
## macOS Bigsur Online Installer with Windows And Mac Users:
**This is a simple and quick summary of the online install USB creation**

Online Windows and macOS Guide:
- **`For Windows users`**
1. Download [rufus](https://rufus.ie/en/)
2. Select the desired flash drive or Sdcard you would like to put the installer on under the device option
3. Select `non-bootable` as the boot selection (REQUIRED)
4. Select `FAT-32` or `Large FAT-32` as the partition scheme and hit start.
- **`For mac users`**
1. Launch Disk Utility
2. `Select View` > `Show all devices` at the top left
3. Select your flash drive (root usb device)and format it as `MS-DOS (FAT)` or `FAT-32`
4.change `guid patition table`-> `Master Boot Record Partiton` and hit start.

5. If in windows,Open up the usb partition in file explorer and delete the files created by rufus.
6. Then ........
7. Create a folder in USB or pendrive or flash drive named `com.apple.recovery.boot`.
8. Now, Install Python from Microsoft store or Download manually for MAC and Windows users here -> [python](https://www.python.org/downloads/) (Make sure you select add python x.x to path for windows users.)
9. Download and extract the [OpenCore Package](https://github.com/acidanthera/OpenCorePkg/releases)
10. Select the "macrecovery" folder in the "opencorepkg" folder at `/Utilities/macrecovery/`
11. Click on home > copy path at the top of file explorer
12. Fire up command prompt or Terminal and type `cd` and hit spacebar and paste the path of the macrecovery folder.
13. Run the command For BigSur: `macrecovery.py -b Mac-42FD25EABCABB274 -m 00000000000000000 download`
- Run the command For Monterey: `macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 download`
14. This will put some files in the macrecovery folder but we only need "BaseSystem.dmg" and "BaseSystem.chunklist" (takes approx. 600mb to 800mb internet)for Downloading the Macos installer.
15. Paste both of those files in the `com.apple.recovery.boot` folder in your flash drive partiton or sdcard or pendrive.
16. Download the latest EFI created [here](https://github.com/devboloji/Infinix-Hackintosh-Guide-Opencore/releases)
17. Copy the folder named `EFI` and paste it in your USB partiton, beside the `com.apple.recovery.boot`

`Note: Make sure to apply the correct bios settings before continuing (provided above)`

17. Restart your laptop and hit `Delete`button continuously until you go to bios settings.
18. Select your flash drive as temporary boot option in boot menu.
19. Now in the OpenCore menu select the name of your USB partiton
Great! Now install and set up macOS Big Sur as usual(This process will be required 14gb internet to download full Macos bigsur). When you are done be sure to read my post install guide.

 # MacOS BigSur Offline Installer from Windows and macOS:
 ### If you don't put the efi after making olarila .raw img, The system will take only 4 to 7mb until insallation. and You can put the efi after booting to the macOS using openocore configurator.
 
- 1.Search and Download Olarila BigSur or Monterey .raw from [Here](https://www.olarila.com/topic/6278-hackintosh-and-macintosh-olarila-vanilla-images-macos/)the latest version of bigsur is 11.6.7 and for Monterey is 12.3.1
- 2.Download etcher from [here](https://www.balena.io/etcher/)
- 3.Make Usb bootable (Flash the Sdcard) using Etcher and olarila bigsur.
- 4.mount the efi of Sdcard or bootable drive.You can watch about mounting the efi in windows[Youtube](https://www.youtube.com/watch?v=-XwKjS6hbwQ) just watch how to select the olarila image from the website and mounting the efi 
- For mac users use Opencore Configurator.app official [here](https://mackie100projects.altervista.org/download-opencore-configurator/)
- Delete the default EFI folder which is in bootable usb
- 5.and paste the Efi to USB. Download Efi [here](https://github.com/devboloji/Infinix-Hackintosh-Guide-Opencore)

- Restart your laptop and hit `Delete`button continuously until you go to bios settings.
- Select your flash drive as temporary boot option in boot menu.
- Now in the OpenCore menu select the name of your USB partiton
 - install.Enjoy!!!!
Restart your laptop and go to bios and reboot from usb.
- 6. Boot to the usb.and install.Enjoy!!!!
Disclaimer - I am not Responsible for any cause of damage for your device.
- You can follow me on [facebook](https://www.facebook.com/sai.dev.92317) and [telegram](https://t.me/Pappusaidev)
<hr>

# Post Install
Once you have verifed that your machine boots properly without any issues as described in the "What Works section", proceed to do the following

### 1. Enable Verbose mode (the black screen with logs on boot up)A real hackintosh Users uses this.
In Config.plist, navigate to NVRAM -> Add -> 7C436110-AB2A-4BBB-A880-FE41995C9F82 -> boot-args and give a single space and add the `-v` argument

### 2. Disable ShowPicker
In the Config.plist, You can disable the boot picker screen so that you boot straight to th Apple logo by setting under `Misc` -> `Boot` -> `ShowPicker` False (NO)
Note: you can still see the boot picker with ShowPicker set to no/false by spamming Esc before the apple logo is displayed during boot.

 ### 3. Boot faster
You can Disable IntelBluetoothFirmware.kext & IntelBluetoothInjector.kext to be able to Boot faster those kexts in config.plist for BigSur.
For Monterey, Disable IntelBluetoothFirmware.kext & Bluetool fixup.kext to be able to Boot faster those kexts in config.plist
This is not done by default to bluetooth working.
***For those on macOS Monterey do not enable IntelBluetoothInjector kext because the system will not boot***
  
### 6. Add Device Properties for Serial number, MLB, ROM, Sytem-UUID and optionally SystemProductName.
Use `MacBookAir9,1` SMBios. Recommended : opencore configurator, Go to the  `PlatformInfo >SMBios`Tick the "Add to the section to config file" in `SMBIOS` and `DATAHUB -GENERIC- PLATFORMNVRAM` and continue your Adding your SMBIOS.
Follow this [Opencore guide](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#generate-a-new-serial) to set up serial number and the accompanying info to get iServices.

                                                                       
Thanks to the OpenCore Team, SAITEJA for testing, also me ofcourse.

