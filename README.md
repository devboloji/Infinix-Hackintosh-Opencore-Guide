| [Releases `+1`](https://github.com/devboloji/Infinix-Hackintosh-Guide-Opencore/releases) | 

## :star_struck: :star_struck: Now the EFI supports Ventura. Sonoma EFI is under development!!:star_struck: :star_struck:
<hr>

### If you people want Sonoma support for our infinix, let me know here.. [Ask here](https://github.com/devboloji/Infinix-Hackintosh-Opencore-Guide/discussions/33#discussion-5280277)

## Infinix-Inbook-series Hackintosh-Guide-Opencore.
- Ice Lake (10th gen) Inbook or X1,slim & x2. Read full guide before you proceed.
### -->[Devboloji](https://github.com/devboloji)-Quote - "think like you have Macbook Air."

<hr>

![img](https://img.shields.io/badge/Release%20Date-Every%20Month-red) ![img](https://img.shields.io/badge/macOS%20Support-Ventura--beta-blue)
![img](https://img.shields.io/badge/macOS%20Support-Monterey--latest-blue)![img](https://img.shields.io/badge/macOS%20Support-BigSur-blue) ![img](https://img.shields.io/badge/OpenCore%20Version-0.8.7-red)

- These are the builts from me.  You might get the future updates for this machine.
 Report me If you find the bugs or any issues. And **don't ask for ETA**(Estimated Time of Time).
- With every EFI update you retrieve from here please remember to go through the **post install guide**(Below)

# :diamond_shape_with_a_dot_inside:buy me a coffee :coffee:  Donate :  :diamond_shape_with_a_dot_inside:

<a href="https://www.paypal.me/369639/"><img src="blue.svg" height="40"></a>  
| <a><img src="darkblue.svg" height="40"></a> |
|-------------------------------------------|
|  `7095160636797@paytm` |

If you enjoyed this project — or just feeling generous, consider buying me a coffee.! :coffee:

 <details><summary>DISCLAIMER</summary>
 
**Disclaimer**
- Hackintoshing may be dangerous and can damage your device and I am not responsible for bricked devices, dead devices, thermonuclear war, or you getting fired because your system failed. Please do some research if you have any concerns about hackintoshing before you proceed. YOU are choosing to make these changes to your system, and if you point the finger at me for messing up your device, I will laugh at you.

 </details>
 
### If you want to report or rasie an ISSUE, you must mention your device details in it. And give a detailed information about your issue(images or videos are encouraged).
 
- You can contact me through [facebook](https://www.facebook.com/sai.dev.92317) and [telegram](https://t.me/Pappusaidev)

 ********************************

## Introduction

**This EFI Only for Single boot users.not for multi-boot users.For multi-boot users need to do some work to work dual boot. Read post-install.**

### [Devboloji](https://github.com/devboloji)-Quote - "think like you have Macbook Air."

# _Device Information_                    

 `Tested Devices`: All (i3,i5,i7)-> Inbook x1, Slim edition, x2.
 
 `Tested CPUs`: **i3-1005G1, i5,i7.**
 
 `Integrated Graphics`:   **G1/G4 , Iris graphics**
 
 `Wireless Cards Tested`: **Intel® AX210.**
  
 `Trackpad`: **Voodoo2IC HID synaptic** 
 
  `Sound Card`: (x1 i3)**ALC269** ->alcid=26 or 99 for i3,
  					(x1 pro-i7)**ALC256** -> alcid=69,
  					x1 slim or x2 = don't know.


 If anyone tested, Let me know: [facebook](https://www.facebook.com/sai.dev.92317) and [telegram](https://t.me/Pappusaidev)
<hr>

## Status : 

**Talking about the battery🔋**, The only issue is when the battery is about 10% or when device shows low battery, don't sleep your device. If you do it, the device may shutdowns or reboots only at that situation.
Note - In this Hacintosh, You get 5hr battery for common usage like using xcode,safari instances, social media apps, and 1080p playback at a time, continuously, simultaneously. **Users** reviews= [see here](https://github.com/devboloji/Infinix-Hackintosh-Opencore-Guide/discussions/24#discussioncomment-4570115)

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
- :heavy_check_mark: Short sleep, Long sleep (If you put your device to sleep for all night, it conusmes 6 to 8 percent. Its common in every operating system
- :heavy_check_mark: For *HDMI* , buy a USB dock not typeC.
- Everything (Much More).

</details>
<details>
 <summary><strong>What's not working ⚠️</strong></summary>
 </br>
 
* :heavy_exclamation_mark: Hdmi slot. To get work, buy a USB Dock.(Try Type-c and usb Type A docks for our infinix) IF the usb Type-C dock works for display out, Inform me.
* :heavy_exclamation_mark: Didn't Mapped Keyboard keys. But it's not mandatory. I like the default keyboard mapping.
* :heavy_exclamation_mark: Audio is dead in x2 or x1 slim due to those devices have intel bluetooth sound cards. But using via headphones or bluetooth or any external audio dongle will work for x2 and x1 slim. Audio is 100% working for x1 and x1 pro.
* :heavy_exclamation_mark: Don't expect too much battery in this Hackintosh like windows. You get atleast 6-hours battery-backup more.
</details>


- The performance is better than windows and linux.(don't check benchmarks with geekbeench. You will see low scores than windows. But in performance, This macOS has great performance than windows, linux. I have tested in different sinarios, You can also test it and let us know about it.

- You definitely get more performance sure than windows without plugin the charge in this MacOS(Hacintosh)... I have tested blender in Both OSes.Blender worked very very smooth than windows(Tested my personal project has "realtime sky Nishita" which puts high work on device with blender 3.2.1.  So you can expect more performance it in My efi. Here, the performace is because of "Metal-Optimisation", but not optimised in "OpenCL" in windows, And we don't need openCL in macos according to me.. Don't except higher performace in gaming like windows & linux in macos


<img align="top" src="images/infinix x1 i3 benchmarks.jpeg" alt="infinx inbook x1 i3 laptop benchmarksimage" width="300">

- **I have also tested the python program benchmark test  (Just used terminal not IDE) : Results:** 

      In windows :
      
        - The program finished compiling on time (on balanced mode)- 4min 36sec.

        - The script finished compiling on time (on performance mode)- 4min 26sec.

      On macOS(hacintosh)without plugging in charge :
         
        - The program finished compiling on time - 4min 16sec.
     
      On Ubuntu 22.04 LTS(original) :
      
        - The program finished compiling on time (on Performance mode)- 4min 39sec.

   Used python 3.9 and This [benchmark script](https://benchmarksgame-team.pages.debian.net/benchmarksgame/program/mandelbrot-python3-7.html) compiled the program x16000 times once.
   
![WindowsVirtualboxBench](https://user-images.githubusercontent.com/87069967/205454534-a03595b8-6aa0-4f0f-8494-1504440f5eca.png)

And also I have tested Windows10 virtualbox with assigning 1core, 4gb ram 50gb storage in macOS monterey. These are the benchmarks.


 <hr>
 

## INSTALLATION

### [Devboloji](https://github.com/devboloji)-Quote - "think like you have Macbook Air."

## Start with bios.

<details>
 <summary><strong> Setting Up with Bios</strong></summary>
 
  Note:Some of these options may not be present in your Bios. If you didn't find some bios, leave it and don't worry about it.
  
<details>
<summary><strong>Disable:</strong></summary>
 
- `chipset` -> `PCH IO configuration` ->`disable wake on wlan and bluetooth` (which causes sleep issues)
- Secure Boot
- `VT-d` -> `Advanced` -> `Cpu` -> `Virtualization technology`
- Disable windows bit-lock encryption (ignore, if you don't lock it, the pre-installed windows doesn't come with bit-lock. Leave it, if you don't know about it.)
 </details>
 
 
<details>
 <summary><strong>Enable:</strong></summary>
 
- `DVMT Total Dfx Mem`(iGPU Memory): `MAX` from `System Agent(SA)configuration` -> `Graphics configuration`.
- Set` DVMT Total Gfx Memory` setting to `Max`from `System Agent(SA)configuration` -> `Graphics configuration`.
- Set `DVMT PPre-Allocated` Setting to `160M` or to `max` from `System Agent(SA)configuration` -> `Graphics configuration`.
- `Intel Virtualization Technology` not vt-d.
</details>

After setting these settings in bios, save it and exit.
</details>

**This is a simple and quick summary of the online install USB creation.**

### macOS Bigsur Installer with Windows And Mac Users:
<details>
 <summary><strong>Process1.MacOS BigSur Online Installer from Windows, linux and macOS:</strong></summary>
 
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
       
  -  **`For Linux users`**
  
  		    1. Install `gparted` and format the usb to `Fat32` and `MBR` OR `MASTER BOOT RECORD PARTITION.
  	    	2. DONE.
  		
6. Then ......................
7. Now, Install Python from Microsoft store or Download manually for MAC,linux and Windows users here -> [python](https://www.python.org/downloads/) (Make sure you select add python x.x to path to environmet variables for windows users.)
8. Download and extract the [OpenCore Package](https://github.com/acidanthera/OpenCorePkg/releases) (Release version is fine).
9. Select the "macrecovery" folder in the "opencorepkg" folder at `/Utilities/macrecovery/` .
10. Copy the path of the "macrecovery" folder in file manager or finder.
11. Fire up command prompt or Terminal and type `cd` and hit spacebar and paste the path of the macrecovery folder.
12.If you cannot run this command, add `python` or `python3` to the beginning of these code.
  - For BigSur  -Run the command: `macrecovery.py -b Mac-42FD25EABCABB274 -m 00000000000000000 download`
  - For Monterey -Run the command: `macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 download`

13. This will download some files in the macrecovery folder but we only need "BaseSystem.dmg" and "BaseSystem.chunklist" (takes approx. 600mb to 800mb internet)for Downloading the Macos installer.
14. Create a folder in USB or pendrive or flash drive named `com.apple.recovery.boot`.
15. Paste both of those files in the `com.apple.recovery.boot` folder in your flash drive partiton or sdcard or pendrive.
16. Download the latest EFI created [here](https://github.com/devboloji/Infinix-Hackintosh-Guide-Opencore/releases)
17. Copy the folder named `EFI` and paste it in your USB partiton.

**Note: If you need to edit Config.plist, don't Clover configurator because its opencore. Use OpenCore configurator , use PlistEdit pro, PropperTree, or Xcode.**

**You will get display glitches only while installing the macOS via USB or any flash drive. But you won't get Atleast ONE glitch after installing of macos or using the MacOS as a daily driver.**

`Note: Make sure to apply the correct bios settings before continuing (provided above)`

 18. Restart your laptop and hit `Delete`button continuously until you go to bios settings.
`Note: Make sure to apply the correct bios settings before continuing (provided above)`
19. Select your flash drive as temporary boot option in boot menu.
20. Now in the OpenCore menu select the name of your USB partiton.
21. Great! Now install and set up macOS Big Sur as usual(This process will be required 14gb internet to download full Macos bigsur).
22. the system reboots for once or twice so, when rebooting choose the usb everytime until you see your Macos Partition name in boot menu.
23. After booting into OS, You need to downlaod opencore configurator and mount the system drive, Then paste the efi to the mounted efi from the USB or drive. then reboot and remove usb.

 </details>
 <details>
  <summary><strong>Process2.MacOS BigSur Offline Installer from Windows and macOS:</strong></summary>
 
- 1.Search and Download Olarila BigSur or Monterey .raw from [Here](https://www.olarila.com/topic/6278-hackintosh-and-macintosh-olarila-vanilla-images-macos/)the latest version of bigsur is 11.xxxx and for Monterey is 12.xxxx
- 2.Download etcher from [here](https://www.balena.io/etcher/)
- 3.Make Usb bootable (Flash the Sdcard) using Etcher and olarila bigsur.
- 4.mount the efi of Sdcard or bootable drive.
- For mac users use Opencore Configurator.app official [here](https://mackie100projects.altervista.org/download-opencore-configurator/)
- 5.Delete the default EFI folder which is in bootable usb
- 6.and paste the Efi to USB. Download Efi [here](https://github.com/devboloji/Infinix-Hackintosh-Guide-Opencore)

**Note: If you need to edit Config.plist, don't Clover configurator because its opencore. Use OpenCore configurator , use PlistEdit pro, PropperTree, or Xcode.**

**You will get display glitches only while installing the macOS via USB or any flash drive. But you won't get Atleast ONE glitch after installing of macos or using the MacOS as a daily driver.**

- 7.Restart your laptop and hit `Delete`button continuously until you go to bios settings.
- 8.Select your sd card or flash drive as temporary boot option in boot menu.
- 9.Now in the OpenCore menu select the name of your USB partiton
- install.Enjoy!!!!

</details>

<details >
 
<summary><strong>After booting in to the *Macos Recovery*</strong></summary>
 

**You may get display glitches only while installing the macOS via USB or any flash drive. But you won't get Atleast ONE glitch after installing of macos or Using the MacOS as a daily driver.**

        - 1. open `Disk Utiliy` -> Select `View` which is at the top left -> choose `Show all devices` -> Select your root of your `SSD drive storage` which you want to install MacOS(root SSD drive device) -> Click `Erase` -> `Name` your drive as you like, Prefered to name as `Macintosh` OR `Macintosh HD` -> change `Format` to `APFS` -> `Scheme` to `Guid Patition Map` -> Click `Erase` .
        - 2. Click `done` and close `disk utility` window. 
        - 3. Select `Install MacOS <macos_version_here>` & click `continue` -> select your `SSD drive name` which you renamed before on Disk Utility and click `continue` .
        - 4. The installer takes 1-3 hours to install for online & offline process.

#### Note : Don't make the screen off, until the installation is over or until the it reboots. If the screen is off in the installation process, it reboots and you need to do the same process of installtion.
 

- After booting into OS, in `setup` you will see `File-Vault` must be disabled or turn-off. After setup,you need to do little work, read post-install-0

</details>

<hr>

# Post Install
Once you have verifed that your machine boots properly without any issues as described in the "What Works section", proceed to do the following

### [Devboloji](https://github.com/devboloji)-Quote - "think like you have Macbook Air."

<details><summary><strong><ins>0. [Must] Boot os without usb or any drive</ins></strong></summary>
 
After booting into OS! So, You need to downlaod opencore configurator [link](https://mackie100projects.altervista.org/opencore-configurator/) -> Open `opencore-configurator`. If it doesn't open, go to `system prefereneces`(Monterey or older) ->  `security`  -> `open anyway`. Open `opencore-configurator` again -> Now mount the `EFI` and paste the `EFI<named-folder>` to the `EFI partition` of your system drive.
 - Remove the USB and reboot. `RESET-NVRAM` once in opencore boot-menu and reboot..Done...

 
</details>

<details><summary><strong><ins>1.Disable the black screen texts on boot up</ins></strong></summary>

( Disabling the Verbose mode)A new hackintosh User uses this. To disable it, In Config.plist, navigate to 'NVRAM' ->  go to Add `7C436110-AB2A-4BBB-A880-FE41995C9F82` -> `boot-args` -> remove the `-v` argument. Save it and reboot. 
 </details>

<details><summary><strong><ins> 2. Disable ShowPicker</ins></strong></summary>
 
Don't use this if you are using dual boot. In the Config.plist, You can disable the boot picker screen so that you boot straight to th Apple logo by setting under `Misc` -> `Boot` -> `ShowPicker` False (NO)
Note: you can still see the boot picker with ShowPicker set to no/false by spamming Esc before the apple logo is displayed during boot.
</details>

<details><summary><strong><ins>3. Boot faster or Remove Volume has MisHash </ins></strong></summary>
If anyone facing Volume Hash Mismatch, Just type `sudo purge` in terminal so you can use bluetooth without rebooting the device.😉
You can Disable IntelBluetoothFirmware.kext & IntelBluetoothInjector.kext to be able to Boot faster those kexts in config.plist for BigSur.
For Monterey, Disable IntelBluetoothFirmware.kext & Bluetool fixup.kext to be able to Boot faster those kexts in config.plist
This is not done by default to bluetooth working.

***For those on macOS Monterey do not enable IntelBluetoothInjector kext because the system will not boot***
</details>  

<details> <summary><strong><ins> 4.Clean Updating your EFI with new EFI release </ins></strong></summary>

To update your EFI with the new Release EFI. The steps:-

1) Download new Release EFI from [here](https://github.com/devboloji/Infinix-Hackintosh-Opencore-Guide/releases) 

2) Take the backup of SMBios or windows dual boot file to other folder, if you required. (if you want to backup SMBIOS,copy `system serial number`, `system UUID`, `MLB`, `ROM`, `System product name`.)

3) Now add those SMBIOS or place Windows EFI files as it should be in old EFI to new EFI, if you backuped before.

4) Mount the EFI partition, Delete the OLD EFI.

5) Copy and paste the new EFI to EFI partition.

6) hit reboot, Remember to do only Reset NVRAM once.

7) Done, you have done a clean EFI Update.

</details>

<details><summary><strong><ins> 5. Add Device Properties for Serial number, MLB, ROM, Sytem-UUID.</ins></strong></summary>
 
Use `MacBookAir9,1` SMBios. Recommended : opencore configurator, Go to the  `PlatformInfo >SMBios`Tick the "Add to the section to config file" in `SMBIOS` and `DATAHUB -GENERIC- PLATFORMNVRAM` and continue your Adding your SMBIOS.
Follow this [Opencore guide](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#generate-a-new-serial) to set up serial number and the accompanying info to get iServices.
 
 Trick to Get exact Processor details in System Information - When you are adding the smbios, Edit `processor type` -> `0` or delete inside of `processor-type` .
 </details>
 
<details><summary><strong><ins> 6.To fix cursor glitch (ignore, if you are done, before installing)</ins></strong></summary>
 
Goto Bios Settings -> `Chipset Section -> System Agent (SA) Configuration -> Graphics Configuration`

Set` DVMT Total Gfx Memory` setting to `Max`
Set `DVMT PPre-Allocated` Setting to `160M` or to `max`
</details>
<details><summary><strong><ins>7.Fix Imessage and Facetime. </ins></strong></summary>
 
If you are new to the apple account or if you are using apple account for the first time in hackintosh, You need to use the apple account for one month and use icloud. Even though, the imessages or factime don't work..
The thing is "Use it" for a month or more and automatically after some days, Magically facetime and imessages workss...Tada...
 </details>
 
 <details><summary><strong><ins> 8.Fix "interface is small" (small text and window issue)</ins></string></summary>
 
- To fix, use [one key high dpi](https://github.com/xzhih/one-key-hidpi) here and run `hidpi.command` in the folder and choose `(1) Enable HIDPI` by typing `1` -> Then choose `Macbook` -> if you want 1920x1080p with best quality use `(4) 2560x1440 Display` or if you want more scale use `(2) 1920x1080 Display (use 1424x802, fix underscaled after sleep)`  or Recommended: for custom resolution -> choose `(6) Manual input resolution` -> then type `1472x828` hit enter -> Reboot your device.
 
-  After rebooting, go to `system Preferences` -> `Display` -> choose `Scaled` and select what you like.
  </details>
 
 <details><summary><strong><ins> 10. Install Windows in Pre-installed MacOS (Dual-Boot). </ins></strong></summary>
 
 - This process is very simple for dual boot and can ask doubts and issues here.
 
 1. Take a Usb or sd-card, connect to pc & Launch `Disk Utility` -> Select `View` > `Show all devices` at the top left.
 2. Select your flash device (root of your usb device)and format it as `MS-DOS (FAT)` or `FAT-32`. Change `guid patition table` -> `Master Boot Record Partiton`. Hit start(by doing this the sdcard formats so you will lose the all the data in sdcard).
 3. Copy the EFI that you are using right now to the `USB` device.
 4. Now download the [Microsoft.zip](https://github.com/devboloji/Infinix-Hackintosh-Opencore-Guide/blob/main/Microsoft.zip) file from my Github and paste the `Microsoft<folder>` inside of `EFI` folder of the USB or sdcard(where you see the `boot`,`OC` folders inside of EFI<folder> in your USb).
 5. Next, to partition your drive, -> Launch `Disk Utility` -> Select `View` > `Show all devices` at the top left -> Choose your `MacOS-drive` as root -> Click `Partition` -> click `add partition` if you see a popup -> `Name` your partition. -> Change the `Format` type to `ExFat` or `Ms-dos` -> Adjust your `Partition size` as you like. click `Apply`. This process takes atleast 15 min. 
 6. Take an Another USB, Now Make bootable of required version of windows by rufus or any other.
 7. Boot to USB from bios. Run the windows Installer as Asusual. But remember to install in your windows Partition in `where to install` in windows disk.
 8. When you boot into windows, install all Updates and you can also restart when updates required reboot.(Forget about macOS for now). After installing all updates, Plug in the `EFI usb` or sdcard(that you previously copied the EFI and Microsoft folders) and reboot to usb from bios to boot into MacOS.
 9. When you boot into MacOS, <ins>Mount the EFI folder</ins>, and Replace default EFI(the drive efi) with your usb or sdcard EFI. Unmount the EFI and reboot.
 10. Try checking the boot menus by Rebooting to macOS & Windows.(you can see "MacOS" & "Windows" in boot-menu)..
 11. Now you can Easily get Windows & MacOS on boot-menu. Enjoy.
 
Thanks to [NitinGaury](https://github.com/nitingaury) for sharing the Dual-boot win&macos in EFI.
 

 . Have a great day. 
 </details>
 
<hr>

Inform me, If there is any error / spelling mistakes in the Installation or any where...    
- You can contact me throught [facebook](https://www.facebook.com/sai.dev.92317) , [telegram](https://t.me/Pappusaidev) , or mail -> saidev949@gmail.com 
## My sincere thanks to**
- ## Thanks for [SaiTeja](https://t.me/Xofficialtech) , he founded and started this Infinix hackintosh project.
- [Acidanthera](https://github.com/acidanthera)
- [Dortania OC guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [CorpNewt's tools](https://github.com/corpnewt)
- Special Thanks to [NitinGaury](https://github.com/nitingaury) for sharing me the Dual-boot win&macOS in EFI.
- [Voodoo2I](https://github.com/VoodooI2C/VoodooI2C)
- [Daliansky's OC-little repo](https://github.com/daliansky/OC-little)
- ### Thanks for [NitinGaury](https://github.com/nitingaury) for helping in making this project possible.
- and the entire community for inspiring me!
