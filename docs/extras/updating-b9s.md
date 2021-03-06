---
title: Updating B9S
---

# Updating B9S
---

## Required Reading

This page is for existing boot9strap users to update their installation of boot9strap to the latest version.

!!! danger "Important"
	While we believe that custom firmware is safe for online use, there have been online network bans in the past, primarily for cheating and suspicious eShop behavior.

## What You Need

* The latest release of [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest)
* The latest release of [boot9strap](https://github.com/SciresM/boot9strap/releases/latest) *(`boot9strap-1.3.zip`; not the `devkit` file, not the `ntr` file)*
* The latest release of [Luma3DS](https://github.com/LumaTeam/Luma3DS/releases/latest)

## Instructions

### Section I - Prep Work

!!! tip ""
	For all steps in this section, overwrite any existing files on your SD card.

1. Insert your SD card into your computer
1. Create a folder named `boot9strap` on the root of your SD card
1. Copy `boot9strap.firm` and `boot9strap.firm.sha` from the boot9strap `.zip` to the `/boot9strap/` folder on your SD card
1. Copy `SafeB9SInstaller.firm` from the SafeB9SInstaller `.zip` to the `/luma/payloads/` folder on your SD card
1. Reinsert your SD card into your device

### Section II - Installing boot9strap

1. Launch Luma3DS chainloader menu by holding (Start) during boot
1. Launch SafeB9SInstaller by pressing (A)
1. Wait for all safety checks to complete
1. When prompted, input the key combo given to install boot9strap
1. Once it has completed, hold (Start) while pressing (A) to reboot your device to the Luma3DS chainloader
    + If you encounter an `argc = 0` error booting your device after the B9S update, just continue to fix it

### Section III - Update Luma3DS

1. Power off your device
1. Insert your SD card into your computer
1. Copy `boot.firm` and `boot.3dsx` from the Luma3DS `.zip` to the root of your SD card, replacing the existing file
1. Reinsert your SD card into your device
1. Power on your device

### Section IV - Configuring Luma3DS

!!! tip ""
	This section is only needed if you are prompted with the Luma3DS configuration menu after the reboot.

1. In the Luma3DS configuration menu, use the (A) button and the D-Pad to turn on the following:    
    + **"Show NAND or user string in System Settings"**
1. Press (Start) to save and reboot

___

!!! tip ""
	### Continue to [Finalizing Setup](../finalizing-setup.md)
