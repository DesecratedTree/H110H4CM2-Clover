# H110-H4-CM2 

![Build](https://i.redd.it/vn2lr3oq2op61.jpg)


## Status

| Component | Status |
| ------ | ------ |
| CPU / Power Management / Sleep | Working |
| Graphics (Nvidia GTX 760) | Working with `WhateverGreen.kext` (Natively supported) |
| USB Ports | Working using `USBMap.kext` & `USBToolbox.kext` |
| Audio - Realtek ALC887 | Working using `-alcid=16` and `AppleALC.kext`  |
| Ethernet - Realtek RTL8111 | Working using `RealtekRTL8111.kext` |
| iServices | iMessage / Facetime not working, iCloud working |
| Dual Boot | Working (using Win10 Pro) |

## Specs

- H110-H4-CM2 Micro ATX Motherboard
- Intel Core i3-6100 @ 3.7GHz
- 16GB (2x8GB) Crucial DDR3L Ram 
- EVGA Nvidia GTX 760 2GB OC Edition
- 1x 500GB PNY SSD (Windows), 1x 400GB Sandisk SSD (MacOS), 1x 2TB Seagate HDD (Shared exFAT drive)
- Rosewill Micro ATX Case
- Dell 22" Monitor, Dell 20" Monitor
- Logitech G Pro Mouse, Redragon K552 Keyboard with Retro Keycaps
- Clover Revision 5135
- macOS Big Sur 11.3 (Probably updated since making this repo)

## Notes
Intel QuickSync does not work due to the motherboard not having an option to enable integrated graphics alongside the GTX 760. VDADecoder fails as well because of this. Seems to have no bearing on actual acceleration. Tested using 3D Chess, Minecraft has full GPU acceleration, RuneLite has full GPU acceleration. DRM does not work with Safari, must use Chrome / Firefox.

## Links

- My Reddit post showcasing the build (https://www.reddit.com/r/hackintosh/comments/meqygs/i36100_gtx760_running_big_sur_1123/)
