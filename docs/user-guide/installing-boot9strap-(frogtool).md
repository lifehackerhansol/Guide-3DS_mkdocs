---
title: Installing boot9strap (Frogtool)
---

# Installing boot9strap (Frogtool)
---

## Required Reading

We will now use our Homebrew Launcher access to run the Frogtool utility in order to inject the exploitable Japanese version of the "Flipnote Studio" title, which we then use to run b9sTool and install boot9strap.

This is a currently working implementation of the "FIRM partitions known-plaintext" exploit detailed [here](https://www.3dbrew.org/wiki/3DS_System_Flaws).

To use the [magnet](https://wikipedia.org/wiki/Magnet_URI_scheme) links on this page, you will need a torrent client like [Deluge](http://dev.deluge-torrent.org/wiki/Download).

## What You Need

* Your `movable.sed` file from completing [Seedminer](seedminer.md)
* <i class="fa fa-magnet" aria-hidden="true" title="This is a magnet link. Use a torrent client to download the file."></i> - [frogcert.bin](magnet:?xt=urn:btih:d12278ea50bb3574f1fbd327f3d0e2292c70941f&dn=frogcert.bin&tr=https%3a%2f%2ftracker.fastdownload.xyz%3a443%2fannounce&tr=https%3a%2f%2fopentracker.xyz%3a443%2fannounce&tr=http%3a%2f%2fopen.trackerlist.xyz%3a80%2fannounce&tr=http%3a%2f%2ft.nyaatracker.com%3a80%2fannounce&tr=udp%3a%2f%2ftracker.tiny-vps.com%3a6969%2fannounce&tr=udp%3a%2f%2fopen.demonii.si%3a1337%2fannounce&tr=udp%3a%2f%2ftracker.port443.xyz%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.vanitycore.co%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.torrent.eu.org%3a451%2fannounce&tr=udp%3a%2f%2fretracker.lanta-net.ru%3a2710%2fannounce&tr=udp%3a%2f%2fthetracker.org%3a80%2fannounce&tr=http%3a%2f%2ftorrent.nwps.ws%3a80%2fannounce&tr=udp%3a%2f%2ftracker.coppersurfer.tk%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.iamhansen.xyz%3a2000%2fannounce&tr=udp%3a%2f%2fbt.xxx-tracker.com%3a2710%2fannounce&tr=http%3a%2f%2f0d.kebhana.mx%3a443%2fannounce&tr=udp%3a%2f%2fexodus.desync.com%3a6969%2fannounce&tr=udp%3a%2f%2ftracker.opentrackr.org%3a1337%2fannounce&tr=udp%3a%2f%2ftracker4.itzmx.com%3a2710%2fannounce&tr=udp%3a%2f%2ftracker.justseed.it%3a1337%2fannounce&tr=http%3a%2f%2ftherightsize.net%3a1337%2fannounce&tr=udp%3a%2f%2fretracker.hotplug.ru%3a2710%2fannounce&tr=udp%3a%2f%2ftracker.internetwarriors.net%3a1337%2fannounce&tr=udp%3a%2f%2f9.rarbg.com%3a2800%2fannounce&tr=https%3a%2f%2f2.track.ga%3a443%2fannounce&tr=udp%3a%2f%2fbigfoot1942.sektori.org%3a6969%2fannounce)
* The latest release of [Frogtool](https://github.com/zoogie/Frogtool/releases/latest)
* The latest release of [b9sTool](https://github.com/zoogie/b9sTool/releases/latest)
* The latest release of [Luma3DS](https://github.com/LumaTeam/Luma3DS/releases/latest)

### Section I - Prep Work

1. Insert your SD card into your computer
1. Copy your `movable.sed` file to the root of your SD card
1. Copy `boot.firm` and `boot.3dsx` from the Luma3DS `.zip` to the root of your SD card
1. Copy `boot.nds` (b9sTool) from the b9sTool release `.zip` to the root of your SD card
1. Copy `Frogtool.3dsx` to the `/3ds/` folder on your SD card
1. Copy `frogcert.bin` to the root of your SD card
1. Reinsert your SD card into your device
1. Power on your device

### Section II - Patching DS Download Play

1. Open the Homebrew Launcher using any method
1. Launch Frogtool from the list of homebrew
1. Select the "INJECT patched DS Download Play" option
1. Frogtool will automatically run and inject the JPN version of Flipnote Studio into your DS Download Play
1. Once this operation has finished, read the screens and check if the process was successful
    + If there are any errors or missing files, correct the problem and try again
1. If the process was successful, tap the touch screen, then select "BOOT patched DS Download Play"
1. If the exploit was successful, your device will have loaded the JPN version of Flipnote Studio

### Section III - Flipnote Exploit

!!! tip "Visual Guide"
	If you would prefer a visual guide to this section, one is available [here](https://zoogie.github.io/web/flipnote_directions/).

1. Complete the initial setup process for the launched game until you reach the main menu
    + Select the left option whenever prompted during the setup process
1. Using the touch-screen, select the large left box, then select the box with an SD card icon
1. Once the menu loads, select the face icon, then the bottom right icon to continue
1. Select the frog icon at the bottom left
    + Alternatively, press (X) or (UP) on the D-Pad depending on which is shown on the top screen
1. Select the second button along the top with a film-reel icon
1. Scroll right until reel "3/3" is selected
1. Tap the third box with the letter "A" in it
1. Scroll left until reel "1/3" is selected
1. Tap the fourth box with the letter "A" in it
1. If the exploit was successful, your device will have loaded b9sTool
1. Using the D-Pad, move to "Install boot9strap"
1. Press (A), then press START and SELECT at the same time to begin the process
1. Once complete and the bottom screen says "done.", exit b9sTool, then power off your device
    + You may have to force power off by holding the power button
    + If you see the Luma configuration menu, continue without powering off

### Section IV - Configuring Luma3DS

1. Boot your device while holding (Select) to launch the Luma configuration menu
    + If you encounter issues launching the Luma configuration menu, [follow this troubleshooting guide](https://github.com/zoogie/b9sTool/blob/master/TROUBLESHOOTING.md)
1. Use the (A) button and the D-Pad to turn on the following:
    + **"Show NAND or user string in System Settings"**
1. Press (Start) to save and reboot
    + Your device should load the Home Menu after a short delay. If you get a black screen lasting longer than 5 minutes, [follow this troubleshooting guide](../troubleshooting.md#black-screen-on-sysnand-boot-after-installing-boot9strap)

### Section V - Restoring DS Download Play

1. Launch the Download Play application (![](/images/download-play-icon.png){: style="height:24px; width:24px"})
1. Wait until you see the two buttons
    + Do not press either of the buttons
1. Press (Left Shoulder) + (D-Pad Down) + (Select) at the same time to open the Rosalina menu
1. Select "Miscellaneous options"
1. Select "Switch the hb. title to the current app."
1. Press (B) to continue
1. Press (B) to return to the Rosalina main menu
1. Press (B) to exit the Rosalina menu
1. Press (Home), then close Download Play
1. Relaunch the Download Play application
1. Your device should load the Homebrew Launcher
1. Launch Frogtool from the list of homebrew
1. Select the "RESTORE patched DS Download Play" option
1. Once this operation has finished, read the screens and check if the process was successful
    + If there are any errors or missing files, correct the problem and try again
1. If the process was successful, tap the touch screen, then press START to exit

!!! tip ""
	### Continue to [Finalizing Setup](../finalizing-setup.md)
