# hp-510-p137cb-efi-hackintosh
EFI Configuration for HP Pavilion 510-p137cb Desktop PC

Compatible with: macOS 10.5.3-10.5.7 Catalina, 11.3.1 (Big Sur)<br>
Not compatible with: Big Sur 11.2.3<br>
Will work for USB installer and OS boot

## How to download and install
Download from the 'Releases' section. Copy the EFI folder to the EFI partition for the macOS installer and/or macOS partition after successful install.<br>
For Big Sur compatibility, download Release 2 or later.

## What to do during installation of macOS
* Go through normal installation

## What to do after successful boot to OS
* Copy the EFI to the EFI partition for the OS
* Generate new SMBIOS data using [Clover Configurator](https://mackie100projects.altervista.org/download-clover-configurator/)
* Remove '-v' flag if text/verbose boot is a bother
* Remove 'dart=0' flag if you do have issues getting VMware or VirtualBox to work
* Set 'Computer Sleep' and 'Display Sleep' to never on System Preferences > Energy Saver if Intel HD Graphics 530
* Uncheck 'Put hard disks to sleep when possible' on System Preferences > Energy Saver if CD/DVD drive is present due to kernel panic

## Hardware Specifications
* <i>Motherboard</i>: Hamar 81B4 (Intel H170 Chipset)
* <i>CPU</i>: Intel Core i5-6400T @ 2.20 GHz
* <i>RAM</i>: 12 GB DDR4-2133 Dual Channel - Samsung HP OEM (1x8GB DS, 1x4GB DS)
* <i>GPU</i>: Intel HD Graphics 530 (Integrated, 1536 MB)
* <i>Video Output</i>: 1 HDMI (VGA port does not work)
* <i>Storage Connection</i>: 2-port SATA III (6.0 Gb/s) - Intel 10 Series Chipset
* <i>Ethernet</i>: Realtek RTL8161 (using RTL8111 kext version 2.2.2)
* <i>Wireless and Bluetooth</i>: Intel Dual-Band Wireless AC 3168 (MVM Gen 1) M.2 Card with BT4.2 USB configuration
* <i>Audio</i>: Realtek HD Audio with DTS Studio (ALC867/ALC3863-CG; use Inject 11 for AppleALC)
* <i>Card Reader</i>: Realtek USB2.0-CRW (unidenified model number)
* <i>USB Connections</i>: 2-port USB 3.0 (rear), 2-port USB 2.0 (rear), 2-port USB 2.0 (front)

## Bootloader Specifications and What is included in the EFI
* <i>Bootloader</i>: Clover ~~r5119~~ r5146 EFI
* <i>SMBIOS Configuration</i>: iMac17,1
* <i>AppleALC</i>: ~~1.7.0~~ 1.7.1
* <i>Lilu</i>: 1.6.0
* <i>WhateverGreen</i>: 1.5.8
* <i>VirtualSMC</i>: 1.2.9
* <i>Realtek RTL8111</i>: 2.2.2
* <i>Intel Bluetooth</i>: 2.1.0

## What is not included in the EFI
* <i>Intel Wireless</i>: Download [itlwm](https://github.com/OpenIntelWireless/itlwm/releases) from GitHub and configure accordingly on the documentation
* <i>Realtek Card Reader</i>: Does not work. Use VMware or VirtualBox with a compatible Linux or Windows OS to use the card reader
