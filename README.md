# MacOS-WLAN-Driver
--------------------
Change your WLAN country code.

Compatible with MacOS X Mojave.

![alt text](https://raw.githubusercontent.com/alessandro893/MacOS-WLAN-Driver/master/wlan_spd.jpg)

802.11d WLAN country code:
--------------------------

- all channels available

- beamforming enabled

- 80mhz enabled on all 5ghz channels

- 1000mw max tx power

![alt text](https://raw.githubusercontent.com/alessandro893/MacOS-WLAN-Driver/master/wlan_info.jpg)

MacOS 10.14.4-10.14.6
--------------------------
Use Modded 10.14.3 'IO80211Family.kext':

https://github.com/alessandro893/MacOS-WLAN-Driver/tree/master/AirPortBrcm4360/10.14.3


MacOS 10.13-10.14.3
--------------------------

1.

Disable 'System Integrity Protection' (csrutil disable)

https://www.macworld.co.uk/how-to/mac/how-turn-off-mac-os-x-system-integrity-protection-rootless-3638975/

2. 

Run in terminal:

sudo perl -pi -e 's|\x41\x83\xFC\xFF\x74\x35\x48\x8D\x55\xD0|\x66\xC7\x06\x55\x53\xEB\x34\x8D\x55\xD0|' /System/Library/Extensions/IO80211Family.kext/Contents/PlugIns/AirPortBrcmNIC.kext/Contents/MacOS/AirPortBrcmNIC

3.

Rebuild Caches (run Kext Utility.app):

https://github.com/alessandro893/MacOS-WLAN-Driver/raw/master/Kext%20Utility.app.zip
