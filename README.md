# MacOS-WLAN-Driver
--------------------
Modified WLAN Drivers with tuned Country Code.


MOD:
--------------------------
<=10.12

- Tuned: RU (Russia) / BY (Belarus) / KZ (Kazakhstan) / DE (Deutschland)

>=10.13

- Hardcoded 'US' Country Code

802.11d WLAN country codes:
--------------------------

-all channels available

-beamforming enabled

-80mhz enabled on all 5ghz channels

-unrestricted max tx power




Via Terminal (>=10.13):
--------------------------

GB:
--------------------------
sudo perl -pi -e 's|\x41\x83\xFC\xFF\x74\x35\x48\x8D\x55\xD0|\x66\xC7\x06\x47\x42\xEB\x34\x8D\x55\xD0|' /System/Library/Extensions/IO80211Family.kext/Contents/PlugIns/AirPortBrcmNIC.kext/Contents/MacOS/AirPortBrcmNIC

US:
--------------------------
sudo perl -pi -e 's|\x41\x83\xFC\xFF\x74\x35\x48\x8D\x55\xD0|\x66\xC7\x06\x55\x53\xEB\x34\x8D\x55\xD0|' /System/Library/Extensions/IO80211Family.kext/Contents/PlugIns/AirPortBrcmNIC.kext/Contents/MacOS/AirPortBrcmNIC
