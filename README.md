# H110H4-CM2 Hackintosh Build

![Build](https://i.redd.it/vn2lr3oq2op61.jpg)


## Status

| Component | Status |
| ------ | ------ |
| CPU / Power Management / Sleep | Working |
| Graphics (Nvidia GTX 760) | Working with `WhateverGreen.kext` (Natively supported) [READ NOTES]|
| USB Ports | Working using `USBMap.kext` & `USBToolbox.kext` |
| Audio - Realtek ALC887 | Working using `-alcid=16` and `AppleALC.kext` |
| Ethernet - Realtek RTL8111 | Working using `RealtekRTL8111.kext` |
| iServices | iMessage / Facetime not working, iCloud working |
| Dual Boot | Working (using Win10 Pro) |
| SMBIOS | Either `iMacPro1,1` or `iMac17,1` works |

## Specs

- H110H4-CM2 Micro ATX Motherboard
- Intel Core i3-6100 @ 3.7GHz
- 16GB (2x8GB) Crucial DDR3L Ram 
- EVGA Nvidia GTX 760 2GB OC Edition
- 1x 500GB PNY SSD (Windows), 1x 400GB Sandisk SSD (MacOS), 1x 2TB Seagate HDD (Shared exFAT drive)
- Rosewill Micro ATX Case
- Dell 22" Monitor, Dell 20" Monitor
- Logitech G Pro Mouse, Redragon K552 Keyboard with Retro Keycaps
- Clover Revision 5135
- macOS Monterey DevBeta1 (had to add `-lilubetaall` to force Lilu.kext to load on beta software)

## Notes
Intel QuickSync does not work due to the motherboard not having an option to enable integrated graphics alongside the GTX 760. VDADecoder fails as well because of this. Seems to have no bearing on actual acceleration. Tested using 3D Chess, Minecraft has full GPU acceleration, RuneLite has full GPU acceleration. DRM does not work with Safari, must use Chrome / Firefox.

YOU MUST CHANGE SERIAL / SMBIOS INFORMATION. I HAVE RANDOMIZED THE SERIAL NUMBER BUT YOU WILL NEED TO USE YOUR OWN OR RANDOMIZE ANOTHER ONE FOR YOURSELF. I AM USING `iMacPro1,1` but `iMac17,1` works if your motherboard supports dual graphics (mine does not). If yours does support dual GPU, set the graphics ID to the proper headless ID to enable QuickSync and dual GPU.

## Benchmarks

| Benchmark | Score |
| ------ | ------ |
| Geekbench CPU Windows | 993pt Single / 2190pt Multi |
| Geekbench GPU Windows | 13303pt |
| Cinebench R23 Windows | 2442pt |
| Geekbench CPU Mac | 911pt Single / 2131pt Multi |
| Geekbench GPU Mac | 4960pt |
| Cinebench R23 Mac | 2415pt |


## Links

- My Reddit post showcasing the build (https://www.reddit.com/r/hackintosh/comments/meqygs/i36100_gtx760_running_big_sur_1123/)
