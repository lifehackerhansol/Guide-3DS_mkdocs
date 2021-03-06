---
title: Installing boot9strap (USM)
---

# Installing boot9strap (USM)
---

## Required Reading

In order to exploit the SAFE_MODE firmware of our system, we need to inject an exploited WiFi profile.

We can do this using an existing exploit, BannerBomb3.

To accomplish this, we use your system's encryption key (movable.sed) to build a DSiWare backup that exploits the system in order to inject the exploited WiFi profile to your connections list.

Once the WiFi profile has been injected, we will use SAFE_MODE, which is a recovery feature present on all 3DS consoles, to activate the exploited WiFi profile.

These instructions work on USA, Europe, Japan, and Korea region consoles as indicated by the letters U, E, J, or K after the system version.

!!! warning "Broken buttons"
	If your (Right/Left Shoulder), (D-Pad Up) or (A) buttons do not work, you will need to use a [Legacy Method](legacy-methods). For assistance with this matter, join [Nintendo Homebrew on Discord](https://discord.gg/MWxPgEp) and ask, in English, for help.

## What You Need

* Your `movable.sed` file from completing [Seedminer](seedminer.md)
* The latest release of [Luma3DS](https://github.com/LumaTeam/Luma3DS/releases/latest)

### Section I - Prep Work

1. If your device is powered on, power off your device
1. Open [unSAFE_MODE-bb3 tool](https://3ds.nhnarwhal.com/3dstools/unsafemode.php) on your computer
1. Upload your movable.sed using the "Choose File" option
1. Click "Download unSAFE_MODE-bb3 archive"
    + This will download an exploit DSiWare called `F00D43D5.bin` and a SAFE_MODE exploit data file called `usm.bin` inside of a zip archive (`unSAFE_MODE-bb3.zip`)
1. Insert your SD card into your computer
1. Copy `boot.firm` and `boot.3dsx` from the Luma3DS `.zip` to the root of your SD card
    + The root of the SD card refers to the initial directory on your SD card where you can see the Nintendo 3DS folder, but are not inside of it
1. Copy `usm.bin` from `unSAFE_MODE-bb3.zip` to the root of your SD card
1. Navigate to `Nintendo 3DS` -> `<ID0>` -> `<ID1>` -> `Nintendo DSiWare` on your SD card
    + The `<ID0>` will be the same one that you used in [Seedminer](seedminer.md)
    + The `<ID1>` is a 32 character long folder inside of the `<ID0>`
    + If `Nintendo DSiWare` does not exist, create it inside of the `<ID1>`
1. If there are any existing DSiWare backup files (`<8-character-id>.bin`) in this folder, move them to your PC
    + This will leave you with an empty Nintendo DSiWare folder. Moving the files to your PC ensures you don't delete any intentional backups
1. Copy the `F00D43D5.bin` file from `unSAFE_MODE-bb3.zip` to the `Nintendo DSiWare` folder

### Section II - BannerBomb3

1. Reinsert your SD card into your device
1. Power on your device
1. Launch System Settings on your device
1. Navigate to `Data Management` -> `DSiWare`
1. Click on the SD Card section
    + Your bottom screen should flash Red and then the system will reboot to home menu a few seconds later. This means the exploit profile was successfully copied
    + If the bottom screen does not flash Red, the exploit profile was not copied and you will not be able to complete the next section. Ensure that your files are properly placed, then try again
1. Power off your device

### Section III - unSAFE_MODE

1. With your device still powered off, hold the following buttons: (Left Shoulder) + (Right Shoulder) + (D-Pad Up) + (A), then press (Power)
    + Keep holding the buttons until the device boots into Safe Mode
1. Press "OK" to accept the update
    + There is no update. This is part of the exploit
1. Press "I accept" to accept the terms and conditions
1. The update will eventually fail, with error code `003-1099`. This is intended behaviour
1. When asked "Would you like to configure Internet settings?", select "Yes"
1. On the following menu, navigate to `Connection 1` -> `Change Settings` -> `Next Page (right arrow)` -> `Proxy Settings` -> `Detailed Setup`
    + This is a [visual representation](/images/screenshots/safemode_highlighted.png)
1. Once you see `B9S install SUCCESS` on the top screen, press any button to reboot to Luma Configuration

### Section IV - Configuring Luma3DS

1. Your device should automatically show the Luma Configuration menu
1. Use the (A) button and the D-Pad to turn on the following:
    + **"Show NAND or user string in System Settings"**
1. Press (Start) to save and reboot
    + Your device should load the Home Menu after a short delay. If you get a black screen lasting longer than 5 minutes, [follow this troubleshooting guide](../troubleshooting.md#black-screen-on-sysnand-boot-after-installing-boot9strap)

### Section V - Restoring WiFi Configuration Profiles

1. Launch System Settings on your device
1. Navigate to `Data Management` -> `DSiWare`
1. Click on the SD Card section
    + Your bottom screen should flash Green and then the system will reboot to home menu a few seconds later. This means your WiFi configuration profiles were successfully restored
1. Power off your device
1. Insert your SD card into your computer
1. Navigate to `Nintendo 3DS` -> `<ID0>` -> `<ID1>` -> `Nintendo DSiWare` on your SD card
1. Delete `F00D43D5.bin` from your Nintendo DSiWare folder

!!! tip ""
	### Continue to [Finalizing Setup](../finalizing-setup.md)
