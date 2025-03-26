# Lenovo Thinkpad E490 Hackintosh - Work in progress!
<p>
    <img style="border-radius: 8px" src="Assets/x.png">
</p>

## System configuration

| Model     | MacBookPro15,2      | Version        | Sequoia 15.3.2      |
| :-------- | :------------------ | :------------- | :------------------ |
| Processor | Intel Core i5-8265U | Graphics       | UHD Graphics 620    |
| Memory    | 2666MHz 2x8GB  | OS Disk        | Samsung 840 EVO SATA SSD |
| Audio     | Conexant CX8070     | WiFi/Bluetooth | Intel Wireless AC9260 (default card)|

## About build

- Based on jamieernest's build for the E490 and https://github.com/5T33Z0/Thinkpad-T490-Hackintosh-OpenCore - attempt to modernize the E490 build for Sequoia.

#### Performance

- Not tested

#### Not Working

Everything

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
- [jamieernest](https://github.com/jamieernest) for the previous build
- [5T33Z0](https://github.com/5T33Z0) for the T490 build
- all other authors that mentioned or not mentioned in this repo
