# Lenovo Thinkpad E490 Hackintosh - Work in progress!
<p>
    <img style="border-radius: 8px" src="Assets/background.png">
</p>

## System configuration

| Model     | MacBookPro15,2      | Version        | Catalina 10.15.7/Big Sur 11.0.1/Monterey 12.3.1      |
| :-------- | :------------------ | :------------- | :------------------ |
| Processor | Intel Core i7-8565U | Graphics       | UHD Graphics 620    |
| Memory    | 2666MHz 2x8GB  | OS Disk        | Crucial MX500 (SATA) (should work with M.2 SSD included with laptop) |
| Audio     | Conexant CX8070     | WiFi/Bluetooth | Intel Wireless AC9260 (default card)|

## About build

- Based on jamieernest's build for the E490 and https://github.com/5T33Z0/Thinkpad-T490-Hackintosh-OpenCore - attempt to modernize the E490 build for Sequoia.

#### Performance

- Not tested

#### Not Working

- Things that may never work:
  - The Fn row functions except volume + brightness control
  - Mixed DRM (for AppleTV+, Netflix and Amazon Prime Video should work)
  - ~~HDMI Port (USB-C works but no video output)~~ Works from Release 0.8.0!

## Installation

### BIOS

Not ready

### STEP

> You can follow [Dortania's guide](https://dortania.github.io/OpenCore-Install-Guide/) as it is very detailed and easy to understand.

#### TL;DR

- Prepare an Mac installer in USB with [GibMacOS](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
- Go to the [releases](https://github.com/jamieernest/Lenovo-E490-Hackintosh/releases) and download the lastest version
- Replace EFI folder in USB EFI partition with the EFI folder from the zip file
- Go into config.plist with [ProperTree](https://github.com/corpnewt/ProperTree) and change the SystemProductName (Type), SystemSerialNumber (Serial), MLB (Board Serial) and SystemUUID (SmUUID) which is generated using [GenSMBIOS.](https://github.com/corpnewt/GenSMBIOS) (Press 1, then 3 then type MacBookPro15,2)
- Boot into USB and select MacOS installer
- In the installer open disk utility and format the SSD to APFS. <strong>YOU WILL LOSE ALL THE DATA THAT IS ON IT</strong> 
- When you are booted in you need to mount EFI partition and replace it with USB's EFI using [Hackintool](https://github.com/headkaze/Hackintool/releases) or [MountEFI](https://github.com/corpnewt/MountEFI)

#### Sleep

Not tested.

## Credits

- [Apple](https://apple.com/) for MacOS
- [acidanthera](https://github.com/acidanthera) for providing almost all kexts and drivers
- [corpnewt](https://github.com/corpnewt) for [GibMacOS](https://github.com/corpnewt/gibMacOS), [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) and [MountEFI](https://github.com/corpnewt/MountEFI)
- [Dortania](https://github.com/dortania) for the [guides](https://dortania.github.io/OpenCore-Install-Guide/)
- [headkaze](https://github.com/headkaze) for providing the very useful [Hackintool](https://github.com/headkaze/Hackintool/releases)
- all other authors that mentioned or not mentioned in this repo
-  and [you](https://cdn.weeb.sh/images/rJl3BcTuG.gif) for reading/following/using this :D
