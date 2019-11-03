# MacOS WLAN Driver for Broadcom 4360
--------------------
Compatible with Mac OS X Catalina ✅

![alt text](https://raw.githubusercontent.com/alessandro893/MacOS-WLAN-Driver/master/wlan_spd.jpg)

802.11d WLAN country code:
--------------------------

- all channels available

- beamforming enabled

- 80mhz enabled on all 5ghz channels

- 1000mw max tx power

![alt text](https://raw.githubusercontent.com/alessandro893/MacOS-WLAN-Driver/master/wlan_info.jpg)

10.14 - 10.15
--------------------------
Easy install:

https://github.com/alessandro893/MacOS-WLAN-Driver/tree/master/App


Manual install:

https://github.com/alessandro893/MacOS-WLAN-Driver/tree/master/AirPortBrcm4360/10.14.3



10.13
--------------------------

1.

Disable 'System Integrity Protection' (csrutil disable)

https://www.macworld.co.uk/how-to/mac/how-turn-off-mac-os-x-system-integrity-protection-rootless-3638975/

2. 

Run in terminal:

sudo perl -pi -e 's|\x41\x83\xFC\xFF\x74\x35\x48\x8D\x55\xD0|\x66\xC7\x06\x55\x53\xEB\x34\x8D\x55\xD0|' /System/Library/Extensions/IO80211Family.kext/Contents/PlugIns/AirPortBrcmNIC.kext/Contents/MacOS/AirPortBrcmNIC

3.

Rebuild Caches & repair permissions

sudo chmod -Rf 755 /System/Library/Extensions/IO80211Family.kext
sudo chown -Rf 0:0 /System/Library/Extensions/IO80211Family.kext
sudo touch /System/Library/Extensions
sudo kextcache -i /
