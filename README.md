# a7y18lte_customization
Compilation of files, tips and tricks and other things to reach the next level of customization

## GoodLock and GoodGuardians
You can use GoodLock on the Samsung Galaxy A7 2018, you can use it with one of the following methods :
- Downloading GoodLock/GoodGuardians directly from the Galaxy Store (requires a Samsung account)
- Downloading FineLock from the playstore (requires a google account)
- Downloading FineLock from your favorite APK downloading website

Here are the available GoodLock apps :
- ThemePark
- LockStar
- ClockFace
- QuickStar
- Wonderland
- NavStar
- One Hand Operation +
- MultiStar
- Sound Assistant
- Routines
- Notistar
- Nice Catch

Here are the available GoodGuardian apps :
- File Guardian
- Battery Tracker
- Battery guardian
- Galaxy App Booster

## Root
It is reccomended to use magisk to root this phone, but due to some change in the way that magisk works and due to how this phone is architectured, __Direct flashing and boot.img patching magisk version other than 21.4 can and will probably lead to problems__.

### Best root apps and modules for this device : 
- #hex_
    - #hex_ is an app that allows you to use the Samsung theming backend at your advantage to make really cool looking themes by yourself. Unfortunately, __this app is dead and won't work on oneUI versions higher than 6.1.1__
- Generic ThemeCenter Patcher
    - Allows you to bypass the trial system of themeCenter, __This reccomendation is meant to bypass the trial bug on #hex, not to use themes without paying, i will not be responsible if a theme dev gets mad at you for using this module__
- Viper4Android
    - Magisk module and app that allows you to customize your sound experience at a level that you probably never imagined
    - Dynamic enhancer bugs out when Sound Assistant's concert room feature is enabled
- Bluetooth Library Patcher
    - Fixes the bluetooth system so that paired devices don't unpair when you reboot
- Global Icon Pack
    - _Requires an Xposed/LsPosed backend_
    - Global Icon Pack is an app that allows you to change the icon pack universally on your system, without even needing a custom launcher
    - For it to work perfectly on your samsung device, it is reccomended to use the following settings :
        - Shared mode
        - Apply to the following apps in your Xposed/LsPosed manager : SystemUI, Settings, Android System, OneUI home screen, Finder, System Maintenance and OneHandOperation+.
- FireFDS kit (Q version)
    - _Requires an Xposed/LsPosed backend_
    - Allows you to tune some weird, but practical settings (like double tap on status bar to sleep, or call recording)


## Custom Recovery
This device only has two custom recoveries : 
- TWRP that can be found [here](https://xdaforums.com/t/recovery-unofficial-twrp-3-7-0-for-galaxy-a7-2018.4718551/)
    - Not reccomended as it can't handle MTP
- PBRP that can be found [here](https://xdaforums.com/t/recovery-unofficial-pbrp-3-1-0-for-galaxy-a7-2018.4280553/)

You can learn how to install a custom recovery from [Here](./Custom%20recovery%20installation.md)

## Bugs, glitches and fixes

### Magisk bootloops device when you install it
This is caused by (not so) recent changes to magisk which causes the device to bootloop, here are the three ways you can still install magisk

<details>
<summary>Patching AP.md5</summary>
You can still have the latest magisk directly out of the box, but it requires reinstalling the stock android.

- Download AP.md5 and put it on your device
- Open magisk app and press install -> Select target file for installation
- Select your AP.md5
- Once it's patched, put it back on your PC and flash it either through odin or heimdall

Your phone will probably ask you to reset since reinstalling the system fucks up the /data encryption
</details>
<details>
<summary>Direct flash through the recovery</summary>
It will require to have magisk version 21.4, then you can flash it directly just like if it was the latest version

When installed, Magisk will ask you to reinstall to finish setting himself up, then it will ask you to update magisk, don't worry, you can do it safely
</details>