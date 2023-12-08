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
- TrackPad with gestures (visible as Magic Trackpad 2)
- Audio, with speaker and microphone support
- QE/CI
- Sleep
- TouchPad buttons
- Multi-Jack (both cold- and hotplug)
- Dedicated brightness control keys (use Fn+S/Fn+B instead) ( F11/12 is working too)

  
<details>

</details>
Pull requests or suggestions are welcome! :)
