## openstip

Openstip is a community effort to complete support for the stip 2 in 1 (stip laptop or tablet) on linux. Currently, only Linux Mint and Void Linux (live iso) have been tested. So far, there is nothing limiting basic usage.

## Existing problems

- No camera support: both the front and back cameras are not recognized at all, due to the /dev/video0 file not existing.
- Broken audio: initially, sound from the speakers sound fine, a bit grainy at best. Then, after just a minute or two, it will be replaced by a monotone screetch. This persisits even in earphones, and restarting pulseaudio with `pulseaudio --kill` seems to be the only solution to stop it. **Note that some apps need to be restarted to play sound once you kill pulseaudio**

## Untested features

- The only stip device we have has a broken screen, so touch capablity has not been tested.
- The boot menu key is unknown (for all we know, it might not even have one). You have to put your usb at the top in the boot settings or choose UEFI booting in the recovery screen to get to boot off of usb.
- Home key has not been tested, broken screen.
- Calling has not been tested, but it probably doesn't work.

## Short tutorial

Get a usb stick (or a "flash"), and download the tool necessary to make your usb bootable. This tutorial uses [ventoy](https://ventoy.net/) as its the easiest, allows multiple iso files on the same usb stick, and you can even keep using the usb as normal after it is bootable. Once you download ventoy, download your linux distro of choice. Linux mint (and by extension, ubuntu), and void linux have been verified to work. Once you download the iso file, make your usb bootable by opening ventoy (in the ventoy folder you extracted from the zip file, Ventoy2Disk.exe for windows, ), clicking on your device in the list and installing ventoy on it. Now all you need to do is copy the linux iso file to the usb like any other file.

Once your usb is ready, turn off the stip, and put the usb in. Then, turn the stip back on while holding the escape key. It should put you in the bios, where you can choose the usb from the list (eg. for example, a sandisk usb will appear as "sandisk"). Go to save and exit, and do so. You should be dropped off in a screen that has the ventoy banner on it, and a list. Select your iso (should be first one, so just click enter) and tap enter again. If any confirmation screens come, just tap enter. You should now come to start installing your linux distro.

**The above is not meant to be a comprehensive guide. Consider reading a typical beginner's guide to installing operating systems if these instructions are too unclear**

## Some minor notes

- The stip is x86-64, not arm64 like a lot of windows tablets. Be thankful.
- Linux shows no indication of switching to "tablet mode" when you remove the keyboard. This is completely normal, linux doesn't bloat itself with things like tablet mode which are useless for most users. If you plan to use it as a tablet, we recommend using gnome as your desktop environment.
 
## How to contribute?
You can contribute to openstip by offering to test your devices, and creating issues whenever you encounter problems.
