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

Here's how to install a custom recovery

0. Check your system
This will check what steps you will require
- Shutdown your phone and then press Power and Vol+ simultaneously until the recovery shows up
    - If you see something that looks like a command line where you navigate using Volume keys, you have the stock recovery and you can follow the checks
    - If you see "LineageOS recovery", the system is already prepped to use a custom recovery, you can skip to step 3
    - If you see something like "TeamWin recovery project" or "PitchBlack recovery project", __STOP__, your system already uses a usable custom recovery and this guide is not necessary
- Boot your phone normally, go to settings -> About this phone -> Software information and go down to "Android system security level"
    - If you see anything other than __November 2020__, you will have to update or downgrade your phone bootloader by following everything
    - If you see __November 2020__, congrats ! You can skip the step 2
- Go into settings -> Developper options and scroll until you find "OEM unlocking"
    - If it's enabled, you can skip step 1
    - If it's disabled, just follow the guide

1. OEM unlock
- In your phone, open the __Settings__ app, then go into developper options
- Scroll down until you find OEM unlock and then press it
    - !!Warning!! Enabling OEM unlocking will reset your phone
- Set up your phone again, __the "finish setting up your phone" notification needs to not be present__
- Now your phone is OEM unlocked !

2. Bootloader downgrade
On your phone
- Shut down your phone
- Press Vol+ and Vol- simultaneously and plug in your phone to your computer

On your computer, __this part will assume that you are on windows__
- Install Samsung USB drivers (if they aren't already)
- Download latest Odin version
- Download November 2020 firmware, we reccomend using [Samfw](https://samfw.com/) as they don't ask a payment for older devices (unlike SamMobile)
- Unpack the zip file
- Open Odin
- Select BL as the BL file you extracted
- In settings, select "Bootloader update"
- Press start

Once it finishes flashing, your phone will reboot, you can now follow the next steps