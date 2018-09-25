# MacOS-WLAN-Driver
--------------------
Change your WLAN country code.

Compatible with MacOS X Mojave.

802.11d WLAN country code:
--------------------------

-all channels available

-beamforming enabled

-80mhz enabled on all 5ghz channels

-unrestricted max tx power




Mod (>=10.13):
--------------------------

TW (Taiwan) 240mw:
--------------------------
sudo perl -pi -e 's|\x41\x83\xFC\xFF\x74\x35\x48\x8D\x55\xD0|\x66\xC7\x06\x54\x57\xEB\x34\x8D\x55\xD0|' /System/Library/Extensions/IO80211Family.kext/Contents/PlugIns/AirPortBrcmNIC.kext/Contents/MacOS/AirPortBrcmNIC

GB (Great Britain) 240mw:
--------------------------
sudo perl -pi -e 's|\x41\x83\xFC\xFF\x74\x35\x48\x8D\x55\xD0|\x66\xC7\x06\x47\x42\xEB\x34\x8D\x55\xD0|' /System/Library/Extensions/IO80211Family.kext/Contents/PlugIns/AirPortBrcmNIC.kext/Contents/MacOS/AirPortBrcmNIC

US (United States) 1000mw:
--------------------------
sudo perl -pi -e 's|\x41\x83\xFC\xFF\x74\x35\x48\x8D\x55\xD0|\x66\xC7\x06\x55\x53\xEB\x34\x8D\x55\xD0|' /System/Library/Extensions/IO80211Family.kext/Contents/PlugIns/AirPortBrcmNIC.kext/Contents/MacOS/AirPortBrcmNIC
