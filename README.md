# Hackintosh for Dell Latitude 3400

---

**NOTE: This was orginally forked from https://github.com/msbence/hackintosh-DellLatitude5400**

---

*Based on OpenCore 0.9.6, of course.*

**WARNING: This repository now uses macOS 13 Ventura, Update to Sonoma using softwareupdate --fetch-full-installer --full-installer-version 14.1.2**

![About my Mac](.img/system.png)

## Specification

| | |
|-|-|
|**CPU**|Intel i5-8265U CPU @ 1.60GHz (Whiskey Lake)|
|**RAM**|8GB DDR4 2400MHz|
|**IGPU**|Intel UHD 620|
|**SSD**|Samsung NVMe 256GB|
|**ETH**|Realtek RTL8111|
|**WLAN+BT**|BCM94360NG (Intel 9560NGW can also work)|
|**Audio**|Realtek ALC236|
|**Ports**|USB-C (PD+DP-AltMode), 3xUSB3.1, HDMI, microSD, Multi-Jack, DC|
|**SMBIOS**|MacBookPro15,2|

## Not working

- HDMI coldplug
- TrackPad with gestures (visible as Magic Trackpad 2)
- MicroSD card reader (Not tested)
- *Hibernation (none of Hackintoshes can do that)*

## Working

- **Everything what is not in the Not working section :D**
- Bluetooth (4.0, LE, Handoff) [out-of-the-box, no kext needed]
- WLAN (Remove Sonoma and rename the orginal AirportItlwm.kext)
- Ethernet (RealtekRTL8111.kext)
- HDMI, DisplayPort Alt Mode (all with sound, but no volume adjustment)
- VGA
- USB ports including USB-C mapped, working after sleep 
- TrackPad (Without gestures)
- Audio, with speaker and microphone support
- QE/CI
- Sleep
- TouchPad buttons
- Multi-Jack (both cold- and hotplug)
- Dedicated brightness control keys (use Fn+S/Fn+B instead)

  
<details>
## Some random text

So I made this hackintosh basically just for fun, but it seems kinda stable, so I use it as my dialy driver. I've never had crashes with it.  

Regarding the not working stuff: with some time I managed to fix almost everything, so only two things are not working, but none of them is a deal-breaker:
 - The brightness control keys are not working, eventhough I added and configured the Brightness Control kext. I kept it, as with a version upgrade they might fix it.
 - HDMI coldplug: I have no idea why is it happing... But I use a USB-C docking station, so it's not a problem at all for me. And the port itself works, just need a re-plugging, so...

I would have a sentence about Intel Wifi+BT which the 5400 contains by default: When I started this project there was no such thing as Intel Wifi support at all. During the years kexts started to appear, and now I have seen promising results. That's why I digged my stock card up, placed it back, and made my EFI compatible with it! So it will work with stock WLAN card. Eventhough I would still recommend getting a natively supported one, first because the Intel card was not so stable (usuable, but not smooth (for example slow network scanning)), secondly as it did with Ventura, Apple can rewrite the whole BT/WLAN with any upgrade. There is nothing better than natively supported hardware, even in this wild west... :)
</details>
Pull requests or suggestions are welcome! :)
