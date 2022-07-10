# dotOSforPixel3
dotOS GSI with fixes for Google Pixel 3 (blueline)

###### ON TESTING, NEW UPDATE EXPECTED ON 11/07/2022

## Important info
This is the GSI build of the ROM, so it is compatible with all the devices supporting Treble, however, all this fixes are **only for Pixel 3** and I am not sure if the would work on other devices

## Instalation
This instructions work only for Pixel devices, and another devices that uses stock fastboot (Xiaomi/POCO/Redmi/etc are not compatible with this proccedure).

###### Fastboot mode
Unlock bootloader
```
$ fastboot flashing unlock
```

Reboot to fastbootd
```
$ fastboot reboot fastboot
```

Erase system partition
```
$ fastboot erase system
```

Erase product partition
```
$ fastboot delete-logical-partition product
```

Flash GSI on a and b slots
```
$ fastboot flash system_a system.img

$ fastboot flash system_b system.img
```

Reboot to bootloader
```
$ fastboot reboot bootloader
```

Erase data and cache
```
$ fastboot -w
```

Done!

###### Flashing NikGapps
On bootloader, flash a recovery like TWRP
```
$ fastboot flash recovery recovery.img
```

When done, reboot to recovery, and install the NikGapps .zip file that's included in the release.
