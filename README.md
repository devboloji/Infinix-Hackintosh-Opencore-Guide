| [Releases `+1`](https://github.com/devboloji/Infinix-Hackintosh-Guide-Opencore/releases) | 

## :star_struck: :star_struck: Now the EFI supports Ventura!!:star_struck: :star_struck:


## Infinix-Hackintosh-Guide-Opencore.
- This repo contains the installation guide and EFI files required to get a perfectly functional of Ventura, Big Sur, Monterey and later Hackintosh on your Ice Lake (10th gen) Inbook or X1,slim. Everything is stable and functional as described in the Readme.

### [Devboloji](https://github.com/devboloji)-Quote - "think like you have Macbook Air."

## ********************************
## This repo is Updated slowly due to lack of Donations and support for this repo. so To support this repo longer, donate. If you donate anytime the repo will be updated faster.
## The current state of this repo is 100% compatible with macOS Ventura, Big Sur & Monterey.
## ********************************

<hr>

- These are the builts from me.  You might get the future updates for this machine.

 - I will try my best to keep the repo updated with the latest kexts and OpenCore version.
 - For macOS Ventura this EFI will work great as BigSur, Monterey. so don't expect flawless functionality.
 Report me If you find the bugs or any issues. And **don't ask for ETA**(Estimated Time of Time).
- With every EFI update you retrieve from here please remember to go through the **post install guide**(Below)

# :diamond_shape_with_a_dot_inside: Donate :diamond_shape_with_a_dot_inside:
|  Any one can donate me or buy me a coffee :coffee:  :|
|--------------------------------------------|
|  via paytm here :`7095160636857@paytm`     |
|  via paypal here: [donate here](https://www.paypal.me/369639)|

 If you ask anyone for EFI they built, They ask you the money. But I am giving the EFI for free to Infinix, There is no result for my Very HardWork and I am giving the Finest EFI by spending Hours by fixing. In Buying a new macbook, I made infinix to Macbook air practically. In-place of buying apple, Donate me to speed up the work for future updates.->[Go to donate session Here](https://github.com/devboloji/Infinix-Hackintosh-Opencore-Guide/edit/main/README.md#diamond_shape_with_a_dot_inside-donate-diamond_shape_with_a_dot_inside)

 <details><summary>DISCLAIMER</summary>
 
|                          Disclaimer                               |
|-------------------------------------------------------------------|
|Read the entire README before you start.                           |
|I am not responsible for any damages you may cause.                |
|If you find an error or improve anything,whether in the config or in the documentation,please consider opening an issue or pull request.|    

 </details>
 
- You can follow me on [facebook](https://www.facebook.com/sai.dev.92317) and [telegram](https://t.me/Pappusaidev) and Telegram support channel:[Support Group](https://t.me/infinix_inbook_discussion)

![img](https://img.shields.io/badge/Release%20Update-July-red) ![img](https://img.shields.io/badge/macOS%20Support-Monterey--11.6.7-blue)![img](https://img.shields.io/badge/macOS%20Support-BigSur-blue) ![img](https://img.shields.io/badge/OpenCore%20Version-0.8.2-red)

## Introduction

EFI folder and Guide for Infinix X1,Slim and Infinix laptop Hackintosh Opencore.

<ins>You can use the latest EFI for Ventura .</ins>
<img align="top" src="images/Ventura beta 5 Proof-Infinix.png" alt="infinx ventura beta 5 system information." width="200">

**Its Only for Single boot users.not for multi-boot users.For multi-boot users need to do some work themselves to work dual boot.**

### [Devboloji](https://github.com/devboloji)-Quote - "think like you have Macbook Air."

<img align="right" src="images/infinix laptop image.jpeg" alt="infinx inbook series laptop image" width="200">

- `Tested CPUs`: **i3-1005G1**

(not tested in i5/i7, If anyone tested, Let me know: [facebook](https://www.facebook.com/sai.dev.92317) and [telegram](https://t.me/Pappusaidev)) and Telegram support channel:[Support Group](https://t.me/infinix_inbook_discussion)


- `Integrated Graphics`: **G1/G4 graphics**

- `Sound Card`: **ALC269 (use alcid=26)** for i3.

- `Wireless Cards Tested`: **Intel® AX210.**

- `Trackpad`: **Voodoo2IC synaptic**

<hr>

### Status : 

- Increased performance than windows and linux.(don't check benchmarks with geekbeench. You will see low scores than windows. But in performance, This macOS has great performance than windows, linux. I have tested in different sinarios, You can also test it and let us know about it in [telegram-group](https://t.me/infinix_inbook_discussion)

- You definitely get more performance sure than windows without plugin the charge in this MacOS(Hacintosh)... I have tested blender in Both OSes.Blender worked very very smooth than windows(Tested my personal project has "realtime sky Nishita" which puts high work on device with blender 3.2.1.  So you can expect more performance it in My efi. Here, the performace is because of "Metal-Optimisation", but not optimised in "OpenCL" in windows, And we don't need openCL in macos according to me..

Note - In this Hacintosh, The cpu is well optimised and you get more performance like you overclocked(by without over-clocking). You get 5hr battery for common usage like using xcode,safari instances, social media apps, and 1080p playback at a time, continuously, simultaneously.

<img align="top" src="images/infinix x1 i3 benchmarks.jpeg" alt="infinx inbook x1 i3 laptop benchmarksimage" width="300">

- #### I have also tested the python program benchmark test  (Just used terminal not IDE) : Results:  

      In windows :
      
        - the program finished compiling on time (on balanced mode)- 4min 36sec.

        - the script finished compiling on time (on performance mode)- 4min 26sec.

      On macOS(hacintosh) :
         
        - the script finished compiling on time - 4min 16sec.
     
      On Ubuntu 22.04 LTS(original) :
        - the script fininshed compiling on time (on Performance mode)- 4min 39sec.

   used this python [benchmark program](https://benchmarksgame-team.pages.debian.net/benchmarksgame/program/mandelbrot-python3-7.html) compiled the program x16000 times once.

#### <ins> Talking about the battery</ins>, The only issue is when the battery is about 15% or when device shows low battery, don't sleep your device. If you do it, the device may shutdowns or reboots only at that situation.

<details>
 <summary><strong> What's working ✅ </strong></summary>
 </br>
 
- :heavy_check_mark: Wifi
- :heavy_check_mark: iMessage, FaceTime, App Store, iTunes Store `Please generate your own SMBIOS`read my [post install](https://github.com/devboloji/Infinix-Hackintosh-Opencore-Guide#post-install) which is below the installation.
- :heavy_check_mark: Bluetooth (Bluetooth Headphones working, also bluetooth file transfer works)
- :heavy_check_mark: OnBoard Audio(Input/ Output)
- :heavy_check_mark: USB ports
- :heavy_check_mark: Wired headphones
- :heavy_check_mark: You will get upto 4 hours to 5 hours battery backup for streaming 1080p-youtube and for coding without any pause.You may get more than me.
- :heavy_check_mark: Trackpad 
- :heavy_check_mark: brightness keys(To increase(+ve) -> `Pause`key) & (To decrease(-ve) -> `Scr Lk` key)
- :heavy_check_mark: Wake / Shutdown
- :heavy_check_mark: Short sleep. (If you make sleep for long hours, The laptop shutdowns. To boot up your device you need to plug in the charge like macbook to wake. But you can make sleep to for 1 to 3 hours(but you will lose 3 to 8 percentage for every hour when  you put your device into sleep). 
This is due to continuous fan spinning when sleep. Anyone is welcomed to fix these issues. First contact me to do that
- :heavy_check_mark: For *HDMI* , buy a USB dock.
- Everything (Much More).

</details>
<details>
 <summary><strong>What's not working ⚠️</strong></summary>
 </br>
 
* :heavy_exclamation_mark: Long Sleep(Using Long sleep, fans still spins and causes battery drain)(Donot use any hibernate app in macos),Read [Post-install](https://github.com/devboloji/Infinix-Hackintosh-Opencore-Guide#post-install) Any one is welcomed to fix this issue, contact me.
* :heavy_exclamation_mark: Hdmi slot. To get work, buy a USB Dock.
* :heavy_exclamation_mark: Don't expect too much battery in this Hackintosh like windows. You get atleast 5-hours battery-backup.
</details>

<details>
 <summary><strong> Setting Up with Bios</strong></summary>
  Note:Most of these options may not be present in your firmware, we recommend matching up as closely as possible but don't be too concerned, if many of these options are not available in your BIOS. You cannot change the cpu,fan and other settings. This is due to Locked-bios(cfg-lock). If anyone unlocked the bios, Please tell in "Telegram-Group" ->(https://t.me/infinix_inbook_discussion) that good news.


<details>
<summary><strong>Disable:</strong></summary>
 
- Fast Boot
- `chipset` -> `PCH IO configuration` ->`disable wake on wlan and bluetooth` (which causes sleep issues)
- Disable windows bit-lock encryption (ignore, if you don't lock it)
- Secure Boot
- VT-d
- CSM
 </details>
 
 
<details>
 <summary><strong>Enable:</strong></summary>
 

- Execute Disable Bit
- `DVMT Total Dfx Mem`(iGPU Memory): `MAX` from `System Agent(SA)configuration` -> `Graphics configuration`.
- Set` DVMT Total Gfx Memory` setting to `Max`from `System Agent(SA)configuration` -> `Graphics configuration`.
- Set `DVMT PPre-Allocated` Setting to `160M` or to `max` from `System Agent(SA)configuration` -> `Graphics configuration`.
- SATA Mode: AHCI
- Every setting is not Available so check your self
- `Intel Virtualization Technology` not vt-d.
</details>
</details>

 <hr>
 

## INSTALLATION

### [Devboloji](https://github.com/devboloji)-Quote - "think like you have Macbook Air."

**This is a simple and quick summary of the online install USB creation.**

You will get display glitches only while installing the macOS via USB or any flash drive. But you won't get Atleast ONE glitch after installing of macos or using the MacOS as a daily driver.
 ### macOS Bigsur Installer with Windows And Mac Users:
<details>
 <summary><strong>Process1.MacOS BigSur Online Installer from Windows and macOS:</strong></summary>
 
  -  **`For Windows users`**
      1. Download [rufus](https://rufus.ie/en/) to format the sdcard to fat32.
      2. Select the desired flash drive or Sdcard you would like to put the installer on under the device option
      3. Open rufus and Select `non-bootable` as the `boot selection` (REQUIRED)
      4. Select `FAT-32` or `Large FAT-32` as the partition scheme. Hit start(by doing this the sdcard formats so you will lose the all the data in sdcard).
      5. If in windows,Open up the usb partition in file explorer and delete all the files created by rufus manually.
  -  **`For mac users`**
      1. Launch `Disk Utility`
      2. `Select View` > `Show all devices` at the top left
      3. Select your flash drive (root usb device)and format it as `MS-DOS (FAT)` or `FAT-32`.
      
      4. change `guid patition table`-> `Master Boot Record Partiton`.
      
      5. hit start(by doing this the sdcard formats so you will lose the all the data in sdcard).

6. Then ................
7. Now, Install Python from Microsoft store or Download manually for MAC and Windows users here -> [python](https://www.python.org/downloads/) (Make sure you select add python x.x to path to environmet variables for windows users.)
8. Download and extract the [OpenCore Package](https://github.com/acidanthera/OpenCorePkg/releases) (Release version is fine).
9. Select the "macrecovery" folder in the "opencorepkg" folder at `/Utilities/macrecovery/` .
10. Copy the path of the "macrecovery" folder in file manager or finder.
11. Fire up command prompt or Terminal and type `cd` and hit spacebar and paste the path of the macrecovery folder.
12.
  - For BigSur  -Run the command: `macrecovery.py -b Mac-42FD25EABCABB274 -m 00000000000000000 download`
  - For Monterey -Run the command: `macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 download`

13. This will download some files in the macrecovery folder but we only need "BaseSystem.dmg" and "BaseSystem.chunklist" (takes approx. 600mb to 800mb internet)for Downloading the Macos installer.
14. Create a folder in USB or pendrive or flash drive named `com.apple.recovery.boot`.
15. Paste both of those files in the `com.apple.recovery.boot` folder in your flash drive partiton or sdcard or pendrive.
16. Download the latest EFI created [here](https://github.com/devboloji/Infinix-Hackintosh-Guide-Opencore/releases)
17. Copy the folder named `EFI` and paste it in your USB partiton.

#### Note: If you need to edit Config.plist, don't Clover configurator because its opencore. Use OpenCore configurator , use PlistEdit pro, PropperTree, or Xcode.
#### You will get display glitches only while installing the macOS via USB or any flash drive. But you won't get Atleast ONE glitch after installing of macos or using the MacOS as a daily driver.

`Note: Make sure to apply the correct bios settings before continuing (provided above)`

 18. Restart your laptop and hit `Delete`button continuously until you go to bios settings.
19. Select your flash drive as temporary boot option in boot menu.
20. Now in the OpenCore menu select the name of your USB partiton.
21. Great! Now install and set up macOS Big Sur as usual(This process will be required 14gb internet to download full Macos bigsur).
22. the system reboots for once or twice so, when rebooting choose the usb everytime until you see your Macos Partition name in boot menu.
23. After booting into OS, You need to downlaod opencore configurator and mount the system drive, Then paste the efi to the mounted efi from the USB or drive. then reboot and remove usb.

 </details>
 <details>
  <summary><strong>Process2.MacOS BigSur Offline Installer from Windows and macOS:</strong></summary>
 
- 1.Search and Download Olarila BigSur or Monterey .raw from [Here](https://www.olarila.com/topic/6278-hackintosh-and-macintosh-olarila-vanilla-images-macos/)the latest version of bigsur is 11.6.7 and for Monterey is 12.3.1
- 2.Download etcher from [here](https://www.balena.io/etcher/)
- 3.Make Usb bootable (Flash the Sdcard) using Etcher and olarila bigsur.
- 4.mount the efi of Sdcard or bootable drive.You can watch about mounting the efi in windows[Youtube](https://www.youtube.com/watch?v=-XwKjS6hbwQ) just watch how to select the olarila image from the website and mounting the efi 
- For mac users use Opencore Configurator.app official [here](https://mackie100projects.altervista.org/download-opencore-configurator/)
- 5.Delete the default EFI folder which is in bootable usb
- 6.and paste the Efi to USB. Download Efi [here](https://github.com/devboloji/Infinix-Hackintosh-Guide-Opencore)

#### Note: If you need to edit Config.plist, don't Clover configurator because its opencore. Use OpenCore configurator , use PlistEdit pro, PropperTree, or Xcode.
#### You will get display glitches only while installing the macOS via USB or any flash drive. But you won't get Atleast ONE glitch after installing of macos or using the MacOS as a daily driver.

- 7.Restart your laptop and hit `Delete`button continuously until you go to bios settings.
- 8.Select your sd card or flash drive as temporary boot option in boot menu.
- 9.Now in the OpenCore menu select the name of your USB partiton
- install.Enjoy!!!!
- 10.After booting into OS, You need to downlaod opencore configurator and mount the system drive, Then paste the efi to the mounted efi from the USB or drive. then reboot and remove usb.

</details>
<hr>

# Post Install
Once you have verifed that your machine boots properly without any issues as described in the "What Works section", proceed to do the following

### [Devboloji](https://github.com/devboloji)-Quote - "think like you have Macbook Air."

<details><summary><strong><ins>0. Boot os without usb or any drive</ins></strong></summary>
 
After booting into OS, You need to downlaod opencore configurator and mount the system drive, Then paste the efi to the mounted efi from the USB or drive. then reboot and remove usb.
</details>

<details><summary><strong><ins>1.Disable the black screen texts on boot up</ins></strong></summary>

( Disabling the Verbose mode)A new hackintosh User uses this. To disable it, In Config.plist, navigate to 'NVRAM' ->  go to Add `7C436110-AB2A-4BBB-A880-FE41995C9F82` -> `boot-args` -> remove the `-v` argument. Save it and reboot. 
 </details>

<details><summary><strong><ins> 2. Disable ShowPicker</ins></strong></summary>
 
In the Config.plist, You can disable the boot picker screen so that you boot straight to th Apple logo by setting under `Misc` -> `Boot` -> `ShowPicker` False (NO)
Note: you can still see the boot picker with ShowPicker set to no/false by spamming Esc before the apple logo is displayed during boot.
</details>

<details><summary><strong><ins>3. Boot faster</ins></strong></summary>
You can Disable IntelBluetoothFirmware.kext & IntelBluetoothInjector.kext to be able to Boot faster those kexts in config.plist for BigSur.
For Monterey, Disable IntelBluetoothFirmware.kext & Bluetool fixup.kext to be able to Boot faster those kexts in config.plist
This is not done by default to bluetooth working.

***For those on macOS Monterey do not enable IntelBluetoothInjector kext because the system will not boot***
</details>  

<details><summary><strong><ins> 4. Add Device Properties for Serial number, MLB, ROM, Sytem-UUID.</ins></strong></summary>
 
Use `MacBookAir9,1` SMBios. Recommended : opencore configurator, Go to the  `PlatformInfo >SMBios`Tick the "Add to the section to config file" in `SMBIOS` and `DATAHUB -GENERIC- PLATFORMNVRAM` and continue your Adding your SMBIOS.
Follow this [Opencore guide](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#generate-a-new-serial) to set up serial number and the accompanying info to get iServices.
 
 Trick to Get exact Processor details in System Information - When you are adding the smbios, Edit `processor type` -> `0` or delete inside of `processor-type` .
 </details>
 
<details><summary><strong><ins> 5.To fix cursor glitch (ignore, if you are done, before installing)</ins></strong></summary>
 
Goto Bios Settings -> `Chipset Section -> System Agent (SA) Configuration -> Graphics Configuration`

Set` DVMT Total Gfx Memory` setting to `Max`
Set `DVMT PPre-Allocated` Setting to `160M` or to `max`
</details>
<details><summary><strong><ins>6.Fix Imessage and Facetime. </ins></strong></summary>
 
If you are new to the apple account or if you are using apple account for the first time in hackintosh, You need to use the apple account for one month and use icloud. Even though, the imessages or factime don't work..
The thing is "Use it" for a month or more and automatically after some days, Magically facetime and imessages workss...Tada...
 </details>
 
 <details><summary><strong><ins> 7.Fix "interface is small" (small text and window issue)</ins></string></summary>
 
- To fix, use [one key high dpi](https://github.com/xzhih/one-key-hidpi) here and run `hidpi.command` in the folder and choose `(1) Enable HIDPI` by typing `1` -> Then choose `Macbook` -> choose  `(2) 1920x1080 Display (use 1424x802, fix underscaled after sleep)` -> Reboot your device.
 
-  After rebooting, go to `system Preferences` -> `Display` -> choose `Scaled` and select what you like.
  </details>
  
<details><summary><strong><ins> 8. Donot try these things in fixing the sleep </ins></strong></summary>
 
 - Donot use any hibernate app in macos.
 - Donot try [opencore sleep fix](https://dortania.github.io/OpenCore-Post-Install/universal/sleep.html#preparations) .
 If you use these! When you put your device sleep, the laptop reboots automatically after 30sec. To fix that you need to reinstall the macOS.
 </details>
 
 <details><summary><strong><ins> 9. Install Windows in Pre-installed MacOS (Dual-Boot). </ins></strong></summary>
 
 - This process is very simple for dual boot and can ask doubts and issues here on [Telegram Group](https://t.me/infinix_inbook_discussion) 
 
 1. Take a Usb or sd-card, connect to pc & Launch `Disk Utility` -> Select `View` > `Show all devices` at the top left.
 2. Select your flash drive (root usb device)and format it as `MS-DOS (FAT)` or `FAT-32`. Change `guid patition table` -> `Master Boot Record Partiton`. Hit start(by doing this the sdcard formats so you will lose the all the data in sdcard).
 3. Copy the EFI that you are using right now to the `USB` or store it to another device.
 4. Next, to partition your drive, -> Launch `Disk Utility` -> Select `View` > `Show all devices` at the top left -> Choose your `MacOS-drive` as root -> Click `Partition` -> click `add partition` if you see a popup -> `Name` your partition. -> Change the `Format` type to `ExFat` or `Ms-dos` -> Adjust your `Partition size` as you like. click `Apply`. This process takes atleast 15 min. 
 5. Take an Another USB, Now Make bootable of required version of windows by rufus or any other.
 6. Boot to USB from bios. Run the windows Installer as Asusual. But remember to install in your windows Partition in `where to install` in windows disk.
 7. When you boot into windows, install all Updates and you can also restart when updates required reboot.(Forget about macOS for now). After installing all updates, Plug in the `EFI usb` and reboot to usb from bios to boot into MacOS.
 8. When you boot into MacOS, <ins>Mount the EFI folder</ins>, and delete `Boot`and `OC` folders and paste the "boot" & "OC" folders from USB to MacOS  EFI. Now go to `Microsoft` -> `Boot` -> change `bootmgfw.efi` to `bootmgfw.efi-ORIG` (replace ".efi" extension to ".efi-ORIG"). Unmount the EFI and reboot.
 9. Reboot to macOS.(you can only see "MacOS" in boot-menu). Now go to `Microsoft` -> `Boot` -> change `bootmgfw.efi-ORIG` to  `bootmgfw.efi` (replace ".efi-ORIG" extension to ".efi" again). Unmount the EFI and reboot.
 10. Now you can see Windows & MacOS on boot-menu. Enjoy. Donation will be helpful : [Here](https://github.com/devboloji/Infinix-Hackintosh-Opencore-Guide#any-one-can-donate-me-or-buy-me-a-coffee-) 
 . Have a great day. 
 </details>
 
<hr>

- You can follow me on [facebook](https://www.facebook.com/sai.dev.92317) and [telegram](https://t.me/Pappusaidev) and Telegram support channel:[Support Group](https://t.me/infinix_inbook_discussion)

 Inform me, If there is any error / spelling mistake in the Installtion or any where...                                                                      
Thanks to the OpenCore Team,Olarila team, SAITEJA for testing, all the hackintosh guides,and me ofcourse.

