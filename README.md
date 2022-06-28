This is the first built from me for BigSur.  You might get the future updates for this machine.

# What's Working.>>
- Sleep / Wake
- Wifi and Bluetooth (bluetooth file transfer works)
-  App Store (see post install guide for more info)
- Onboard audio
- USB 2.0 / USB 3.0
- USB 2.0 / USB 3.0
- Everything (Much More).

## <What's Not working>
* iMessages, Facetime.
* This Update is for BigSur 11.6.7, and not for Monterey or More.

# Introduction
EFI folder and Guide for Infinix_INBook_X1 i3 1005G1 8gb,256gb BigSur.

Tested CPUs: i3 1005G1 10gen
Integrated Graphics: UHD G1
Sound Card: ALC269
Wireless Cards Tested: [Intel® Wi-Fi 6E AX210.

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
1.Download [rufus](https://rufus.ie/en/)
2.Select the desired flash drive you would like to put the installer on under the device option
3.Select non-bootable as the boot selection (REQUIRED)
4.Select FAT-32 or Large FAT-32 as the partition scheme
5.Open up the usb partition in file explorer and delete the files created by rufus
6.Create a folder on that partiton named com.apple.recovery.boot
7.Install [python](https://www.python.org/downloads/) (Make sure you select add python x.x to path)
8.Download and extract the [OpenCore Package](https://github.com/acidanthera/OpenCorePkg/releases)
9.Select the macrecovery folder in the opencorepkg folder at>  /Utilities/macrecovery/
10.Click on home > copy path at the top of file explorer
11.Fire up command prompt and type cd and hit spacebar and paste the path of the macrecovery folder.
12.Run the command:
 python macrecovery.py -b Mac-42FD25EABCABB274 -m 00000000000000000 
download starts.
13.This will put some files in the macrecovery folder but we only need BaseSystem.dmg and BaseSystem.chunklist
14.Paste both of those files in the> com.apple.recovery.boot < folder in your flash drive partiton
15.Download the latest EFI created [here](https://github.com/racka98/Lenovo-Thinkpad-T450-T450s-Hackintosh-Guide-Opencore/releases)
16.Copy the EFI folder and paste it in your USB partiton
Note: Make sure to apply the correct bios settings before continuing (provided above)

**Full Changelog**: https://github.com/devboloji/Infinix_INBook_X1_XL11_i3-Hackintosh-Guide-Opencore/commits/v1.0

Thanks to the OpenCore Team, Olarila Team, SAITEJA, AMD Team, Mieze, btwise, and also me ofcourse.

