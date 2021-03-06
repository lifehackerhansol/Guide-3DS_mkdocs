---
title: Installing boot9strap (Soundhax)
---

# Installing boot9strap (Soundhax)
---

## Required Reading

Soundhax (when combined with universal-otherapp) is compatible with versions 1.0.0 through 11.3.0 in all regions.

## What You Need

- The latest release of [Soundhax](http://soundhax.com) *(for your region, device, and version)*
    - If Soundhax appears in your browser as an unplayable video, press Ctrl+S or Cmd+S to save it to your computer
- The latest release of [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/latest)
- The latest release of [boot9strap](https://github.com/SciresM/boot9strap/releases/latest) *(`boot9strap-1.3.zip`; not the `devkit` file, not the `ntr` file)*
- The latest release of [Luma3DS](https://github.com/LumaTeam/Luma3DS/releases/latest)
- The latest release of [universal-otherapp](https://github.com/TuxSH/universal-otherapp/releases/latest)

## Instructions

### Section I - Prep Work

1. Power off your device
1. Insert your SD card into your computer
1. Copy the Soundhax `.m4a` to the root of your SD card
1. Copy `otherapp.bin` to the root of your SD card
1. Copy `boot.firm` and `boot.3dsx` from the Luma3DS `.zip` to the root of your SD card
1. Create a folder named `boot9strap` on the root of your SD card
1. Copy `boot9strap.firm` and `boot9strap.firm.sha` from the boot9strap `.zip` to the `/boot9strap/` folder on your SD card
1. Copy `SafeB9SInstaller.bin` from the SafeB9SInstaller `.zip` to the root of your SD card
1. Reinsert your SD card into your device
1. Power on your device

### Section II - Launching SafeB9SInstaller

1. Reinsert your SD card into your device
1. Power on your device
1. Launch Nintendo 3DS Sound

!!! tip ""
	![Welcome Screen](/images/screenshots/soundhax-welcome.png)

1. If you've never opened Nintendo 3DS Sound before and get tips on how to use it from a bird icon, go through all of the bird tips, then close the app normally and relaunch it
    - In this situation, launching Soundhax immediately would cause these tips to appear on every launch of the Nintendo 3DS Sound until this is done
1. Go to `/SDCARD`, then play "<3 nedwill 2016"
    - This may take many tries
    - If it freezes, force the console to power off by holding the power button, then try again
    - If your console displays a red and white screen *and* your console is on system version 9.4.0, 9.5.0, or 9.6.0, try following [Homebrew Launcher (Soundhax)](homebrew-launcher-(soundhax).md)

!!! tip ""
	![Launching Soundhax](/images/screenshots/soundhax-launch.png)

1. If the exploit was successful, you will have booted into SafeB9SInstaller

### Section III - Installing boot9strap

1. Wait for all checks to complete
1. When prompted, input the key combo given on the top screen to install boot9strap
1. Once it has completed, press (A) to reboot your device

### Section IV - Configuring Luma3DS

1. Your device should have rebooted into the Luma3DS configuration menu
    - If you get a black screen, [follow this troubleshooting guide](../troubleshooting.md#black-screen-on-sysnand-boot-after-installing-boot9strap)
1. Use the (A) button and the D-Pad to turn on the following:
    - **"Show NAND or user string in System Settings"**
1. Press (Start) to save and reboot
    - If you get an error, just continue the next page

___

!!! tip ""
	### Continue to [Finalizing Setup](../finalizing-setup.md)

