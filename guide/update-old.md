<img align="right" src="https://github.com/n00b69/woa-polaris/blob/main/polaris.png" width="350" alt="Windows 11 running on polaris">

# Running Windows on the Xiaomi Mix 2s

## Updating drivers (old method)

### Prerequisites
- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)
  
- [Drivers](https://github.com/n00b69/woa-POLARIS/releases/tag/Drivers)
  
- [UEFI image](https://github.com/n00b69/woa-polaris/releases/tag/UEFI)

### Boot to OFOX recovery
> If your recovery has been replaced by the stock recovery, flash it again using
```cmd
fastboot flash recovery path\to\ofox.img reboot recovery
```

#### Enabling mass storage mode
> If it asks you to run it once again, do so
```cmd
adb shell msc
```
### Diskpart
```cmd
diskpart
```

#### List device volumes
> To print a list of all the connected volumes, run
```cmd
list volume
```

#### Select Windows volume
> Replace $ with the actual number of **WINPOLARIS**
```cmd
select volume $
```

#### Assign letter to WINF1
```cmd
assign letter x
```

#### Exit diskpart
```cmd
exit
```

### Installing Drivers
> Unpack the driver archive, then open the `OfflineUpdater.cmd` file

> Enter the drive letter of **WINPOLARIS**, which should be X, then press enter

#### Boot back into Windows
> Reboot your device to boot back into Windows. If this boots you to Android, reflash the UEFI image through fastboot or by using the WOA Helper app


## Finished!


















