# Worked/Works with: MacOS 15.4.1
> This is absolutely not guaranteed to work for you, it's kinda here for backup reasons

- **Motherboard:** ASRock Fatal1ty B360 Gaming K4
- **BIOS settings:** as shown in the [guide](https://dortania.github.io/OpenCore-Install-Guide/config.plist/coffee-lake.html#intel-bios-settings)
- **CPU:** Intel Core i5-9400F
- **GPU:** AMD Radeon RX 6700 XT (12G) (Gigabyte) (Navi22)
- **RAM:** 2x8gb, 2666mhz, DDR4
- **PSU:** 750W
- **Display:** LG MP59G, HDMI
- **Drive:** WD black sn750, 500gb
- **Installed next to Win11 on the same nvme drive**
- **Uses NootRX, hardware acceleration works**
- **Audio works with both alcid 3 and 5, the rest are untested**
- **iServices seem to work**

# Installation
- ### [Read the guide!!](https://dortania.github.io/OpenCore-Install-Guide/)
- tl;dr:
  - your drive MUST be GPT!
  - have an 80+gb partition formatted to exFat
    - *(when the partition was uncallocated, it didnt work, probably because of the windows disk management)*
  - format a usb drive as non-bootable with [Rufus](https://rufus.ie/)
  - boot to the usb, erase the partition in the recovery mode, then install MacOS
  - mount efi partition in MacOS, or use [EasyUEFI](https://www.easyuefi.com/index-us.html) on windows
  - move the OC folder from the usb drive to `.\EFI\`
    - *(you should have `.\EFI\OC\...`)*
    - *(on Windows, I also had to add a new boot option in EasyUEFI, not sure on MacOS)*
  - put opencore as the #1 boot option in your bios
