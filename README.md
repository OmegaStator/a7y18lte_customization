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
    - Allows you to bypass the trial system of themeCenter, __This reccomendation is meant to bypass the trial bug on #hex_, not to use themes without paying, i will not be responsible if a theme dev gets mad at you for using this module__
- Viper4Android
    - Magisk module and app that allows you to customize your sound experience even more
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