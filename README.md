| [Releases `+1`](https://github.com/devboloji/Infinix-Hackintosh-Guide-Opencore/releases) |


## Infinix-Hackintosh-Guide-Opencore.
- This repo contains the installation guide and EFI files required to get a perfectly functional of Big Sur and later Hackintosh on your Ice Lake (10th gen) Inbook or X1,slim. Everything is stable and functional as described in the Readme.

# ********************************
# This repo is no longer Updated due to lack of Donations and support for this repo. so I can no longer offer support for this. If you donate anytime the repo will be updated.
# This repo will archived and all open issues are closed
# The current state of this repo is 100% compatible with macOS Big Sur & Monterey.
# ********************************

<hr>

- These are the builts from me.  You might get the future updates for this machine.

 - I will try my best to keep the repo updated with the latest kexts and OpenCore version.
 - For macOS Monterey this EFI will work great as BigSur. so don't expect flawless functionality
Report me If you find the bugs or any issues. And don't ask for ETA(Estimated Time of Time).
- With every EFI update you retrieve from here please remember to go through the **post install guide**(Below)

# Any one can donate me or buy me a coffee :
#### via paytm here :`7095160636857@paytm`
#### via paypal here: [donate here](https://www.paypal.me/369639)
 <details><summary>DISCLAIMER</summary>
 
|                          Disclaimer                               |
|-------------------------------------------------------------------|
|Read the entire README before you start.                           |
|I am not responsible for any damages you may cause.                |
|- Should you find an error or improve anything,whether in the config or in the documentation,please consider opening an issue or pull request.|    

 </details>
 
- You can follow me on [facebook](https://www.facebook.com/sai.dev.92317) and [telegram](https://t.me/Pappusaidev) and Telegram support channel:[Support Group](https://t.me/infinix_inbook_discussion)

![img](https://img.shields.io/badge/Release%20Update-July-red) ![img](https://img.shields.io/badge/macOS%20Support-Monterey--11.6.7-blue)![img](https://img.shields.io/badge/macOS%20Support-BigSur-blue) ![img](https://img.shields.io/badge/OpenCore%20Version-0.8.2-red)

## Introduction

EFI folder and Guide for Infinix X1,Slim and Infinix laptop Hackintosh Opencore.
**Its Only for Single boot users.not for multi-boot users.For multi-boot users need to do some work themselves to work dual boot.**

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

- You definitely get more performance sure than windows without plugin the charge in this MacOS(Hacintosh)..I have tested blender in Both OSes.Blender worked very very smooth than windows(Tested my personal project has "realtime sky Nishita" which puts high work on device with blender 3.2.1.  So you can expect more performance it in My efi. Here, the performace is because of "Metal-Optimisation", but not optimised in "OpenCL" in windows , And we don't need openCL in macos according to me..

Note - In this Hacintosh, The cpu is well optimised and you get more performance like you overclocked(without over-clocking). You get 5hr battery for common usage like using xcode,safari instances, social media apps, and 1080p playback at a time, continuously.

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

<details>
 <summary><strong> What's working ✅ </strong></summary>
 </br>
 
- [x] Wifi
- [x] iMessage, FaceTime, App Store, iTunes Store `Please generate your own SMBIOS`read my [post install](https://github.com/devboloji/Infinix-Hackintosh-Opencore-Guide#post-install) which is below the installation.
- [x] Bluetooth (Bluetooth Headphones working, also bluetooth file transfer works)
- [x] OnBoard Audio(Input/ Output)
- [x] USB ports
- [x] Wired headphones
- [x] You will get upto 3 1/2 hours to 4 hours battery backup for streaming 1080p-youtube and for coding without any pause.You may get more than me.
- [x] Trackpad 
- [x] brightness keys(To increase(+ve) -> `Pause`key) & (To decrease(-ve) -> `Scr Lk` key)
- [x] Wake / Shutdown
- [x] Short sleep. (If you make sleep for long hours, The laptop shutdowns. To boot up your device you need to plug in the charge like macbook to wake. But you can make sleep to for 1 to 3 hours(but you will lose 2 to 3 percentage for every hour when  you put your device into sleep.) 
This is due to continuous fan spinning when sleep. Anyone is welcomed to fix these issues. First contact me to do that
- Everything (Much More).

</details>
<details>
 <summary><strong>What's not working ⚠️</strong></summary>
 </br>
 
* Long Sleep(Using Long sleep, fans still spins and causes battery drain)(Donot use any hibernate app in macos) Any one is welcomed to fix this issue, contact me.
* Hdmi slot.
* Don't expect too much battery in this Hackintosh like windows. You get atleast 5-hours battery-backup.
</details>

<details>
 <summary><strong> Setting Up with Bios</strong></summary>
  Note:Most of these options may not be present in your firmware, we recommend matching up as closely as possible but don't be too concerned if many of these options are not available in your BIOS. You cannot change the cpu,fan and other settings. This is due to Locked-bios(cfg-lock). If anyone unlocked the bios, Please tell that good news in [telegram-Group](https://t.me/infinix_inbook_discussion). 
 <details>
<summary><strong>Disable:</strong></summary>
 
- Fast Boot
- disable wake on wlan and bluetooth (which causes sleep issues)
- Disable windows bit-lock encryption (ignore, if you don't lock it)
- Secure Boot
- Serial/COM Port
- Parallel Port(if you have)
- VT-d (can be enabled if you set DisableIoMapper to YES)
- CSM
- Thunderbolt(For initial install, as Thunderbolt can cause issues if not setup correctly)
- Intel Platform Trust (if you don't see in bios, leave it)
- CFG Lock (MSR 0xE2 write protection)(This must be off, if you can't find the option then enable AppleXcpmCfgLock under Kernel -> Quirks. Your hack will not boot with CFG-Lock enabled)
 </details>
<details>
 <summary><strong>Enable:</strong></summary>
 
- VT-x
- Above 4G decoding(if you don't see in bios, leave it)
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- DVMT Pre-Allocated(iGPU Memory): 256MB or MAX
- Set` DVMT Total Gfx Memory` setting to `Max`
- Set `DVMT PPre-Allocated` Setting to `160M` or to `max`
- SATA Mode: AHCI
- Every setting is not Available so check your self
- Intel Virtualization Technology.
</details>
</details>

 <hr>
 

## INSTALLATION
**This is a simple and quick summary of the online install USB creation**
You will get display glitches only while installing the macOS via USB or any flash drive. But you won't get Atleast ONE glitch after installing of macos or using the MacOS as a daily driver.
 ### macOS Bigsur Installer with Windows And Mac Users:
<details>
 <summary><strong>Process1.MacOS BigSur Online Installer from Windows and macOS:</strong></summary>
 
- **`For Windows users`**
1. Download [rufus](https://rufus.ie/en/)
2. Select the desired flash drive or Sdcard you would like to put the installer on under the device option
3. Open rufus and Select `non-bootable` as the `boot selection` (REQUIRED)
4. Select `FAT-32` or `Large FAT-32` as the partition scheme. Hit start(by doing this the sdcard formats so you will lose the all the data in sdcard).
5. If in windows,Open up the usb partition in file explorer and delete all the files created by rufus manually.
- **`For mac users`**
1. Launch `Disk Utility`
2. `Select View` > `Show all devices` at the top left
3. Select your flash drive (root usb device)and format it as `MS-DOS (FAT)` or `FAT-32`
4.change `guid patition table`-> `Master Boot Record Partiton`.
5.hit start(by doing this the sdcard formats so you will lose the all the data in sdcard).

6. Then ........
7. Now, Install Python from Microsoft store or Download manually for MAC and Windows users here -> [python](https://www.python.org/downloads/) (Make sure you select add python x.x to path to environmet variables for windows users.)
8. Download and extract the [OpenCore Package](https://github.com/acidanthera/OpenCorePkg/releases) (Release version is fine).
9.Select the "macrecovery" folder in the "opencorepkg" folder at `/Utilities/macrecovery/`
10.Copy the path of the "macrecovery" folder in file manager or finder.
11.Fire up command prompt or Terminal and type `cd` and hit spacebar and paste the path of the macrecovery folder.
12.For BigSur  -Run the command: `macrecovery.py -b Mac-42FD25EABCABB274 -m 00000000000000000 download`
- For Monterey -Run the command: `macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 download`

13. This will download some files in the macrecovery folder but we only need "BaseSystem.dmg" and "BaseSystem.chunklist" (takes approx. 600mb to 800mb internet)for Downloading the Macos installer.
14.Create a folder in USB or pendrive or flash drive named `com.apple.recovery.boot`.
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
  <summary><strong>process2.MacOS BigSur Offline Installer from Windows and macOS:</strong></summary>
 
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

<details><summary><strong>0. Boot os without usb or any drive</strong></summary>
 
After booting into OS, You need to downlaod opencore configurator and mount the system drive, Then paste the efi to the mounted efi from the USB or drive. then reboot and remove usb.
</details>

<details><summary><strong>1.Fix the black screen texts on boot up</strong></summary>

( Enabling Verbose mode)A real hackintosh User uses this. To enable it, In Config.plist, navigate to NVRAM -> Add -> `7C436110-AB2A-4BBB-A880-FE41995C9F82` -> `boot-args` and give a single space and add the `-v` argument.
 </details>

<details><summary><strong> 2. Disable ShowPicker</strong></summary>
 
In the Config.plist, You can disable the boot picker screen so that you boot straight to th Apple logo by setting under `Misc` -> `Boot` -> `ShowPicker` False (NO)
Note: you can still see the boot picker with ShowPicker set to no/false by spamming Esc before the apple logo is displayed during boot.
</details>

<details><summary><strong>3. Boot faster</strong></summary>
You can Disable IntelBluetoothFirmware.kext & IntelBluetoothInjector.kext to be able to Boot faster those kexts in config.plist for BigSur.
For Monterey, Disable IntelBluetoothFirmware.kext & Bluetool fixup.kext to be able to Boot faster those kexts in config.plist
This is not done by default to bluetooth working.

***For those on macOS Monterey do not enable IntelBluetoothInjector kext because the system will not boot***
</details>  

<details><summary><strong> 4. Add Device Properties for Serial number, MLB, ROM, Sytem-UUID.</strong></summary>
 
Use `MacBookAir9,1` SMBios. Recommended : opencore configurator, Go to the  `PlatformInfo >SMBios`Tick the "Add to the section to config file" in `SMBIOS` and `DATAHUB -GENERIC- PLATFORMNVRAM` and continue your Adding your SMBIOS.
Follow this [Opencore guide](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#generate-a-new-serial) to set up serial number and the accompanying info to get iServices.
 </details>
 
<details><summary><strong> 5.To fix cursor glitch (ignore,if you are done, before installing)</strong></summary>
 
Goto Bios Settings -> `Chipset Section -> System Agent (SA) Configuration -> Graphics Configuration`

Set` DVMT Total Gfx Memory` setting to `Max`
Set `DVMT PPre-Allocated` Setting to `160M` or to `max`
</details>
<details><summary><strong>6.Fix Imessage and Facetime</strong></summary>
 
If you are new to the apple account or if you are using apple account for the first time in hackintosh, You need to use the apple account for one month and use icloud. Even though, the imessages or factime don't work..
The thing is "Use it" for a month or more and automatically after some days, Magically facetime and imessages workss...Tada...
 </details>
 
 <details><summary><strong> 7.Fix "interface is small" (small text and window issue)</string></summary>
 
- To fix, use [one key high dpi](https://github.com/xzhih/one-key-hidpi) here and run `hidpi.command` in the folder and choose `(1) Enable HIDPI` by typing `1` -> Then choose `Macbook` -> choose  `(2) 1920x1080 Display (use 1424x802, fix underscaled after sleep)` -> Reboot your device.
 
-  After rebooting, go to `system Preferences` -> `Display` -> choose `Scaled` and select what you like.
  </details>
  
<hr>

- You can follow me on [facebook](https://www.facebook.com/sai.dev.92317) and [telegram](https://t.me/Pappusaidev) and Telegram support channel:[Support Group](https://t.me/Infinix_Inbook_discussion)

 Inform me, If there is any spelling mistake in the Installtion or any where...                                                                      
Thanks to the OpenCore Team, SAITEJA for testing, also me ofcourse.

