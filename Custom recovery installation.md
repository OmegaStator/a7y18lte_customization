
# How to install a custom recovery on a7y18lte

### 0. Check your system
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
---
### 1. OEM unlock
- In your phone, open the __Settings__ app, then go into developper options
- Scroll down until you find OEM unlock and then press it
    - !!Warning!! Enabling OEM unlocking will reset your phone
- Set up your phone again, __the "finish setting up your phone" notification needs to not be present__
- Now your phone is OEM unlocked !

---
### 2. Bootloader downgrade
__WARNING : Bootloader downgrade is limited to the bit rev, if you are on bit rev *5*, you can't downgrade to bootloaders that have a lower bit rev__


On your phone
- Shut down your phone
- Press Vol+ and Vol- simultaneously and plug in your phone to your computer

On your computer, __this part will assume that you are on windows__
- Install Samsung USB drivers (if they aren't already installed)
- Download latest Odin version
- Download November 2020 firmware, we reccomend using [Samfw](https://samfw.com/) as they don't ask a payment for older devices (unlike SamMobile)
- Unpack the zip file
- Open Odin
- Select BL as the BL file you extracted
- In the "settings" tab, select "Bootloader update"
- Press start

Once it finishes flashing, your phone will reboot, you can now follow the next steps

---
### 3. Custom recovery installation
On your phone
- Shut down your phone
- Press Vol+ and Vol- simultaneously and plug in your phone to your computer

On your computer, __this part will assume that you are on windows__
- Install Samsung USB drivers (if they aren't already installed)
- Download latest Odin version
- Download the custom recovery you choose (either Lineage recovery for LineageOS 18.1, TWRP or PBRP)
- Unpack the zip file, there should be a recovery.img somewhere
- zip the recovery.img into a tar archive
- Open Odin and select the newly created recovery.tar as AP
- Go to "settings" tab and uncheck "Auto reboot"
- Press start to start the flash
- Once Odin says "Pass" with a green background, press Vol- and Power at the same time and immediately switch to Vol+ and Power once the download mode screen is gone
- You should be greeted by your custom recovery, don't worry, it will patch the system automatically so that the OS recovery doesn't overwrite your custom recovery
---
### 4. Access internal storage and /data from recovery
You probably noticed something weird when entering your custom recovery : it doesn't report your full storage in MTP and only reports something like ~11Gb

This is caused by encryption, this phone encrypts _/data_ by default, here's how to unencrypt it

- Shut down your phone
- Press Vol+ and Power to start to the custom recovery
- Once in your custom recovery, press "wipe" to enter wipe menu
- You should be greeted with a "reset data" option, swipe to wipe and write "yes" in the text box, your /data directory will be formatted, please note that doing so will delete __ALL YOUR DATA__ (Apps, app data and internal storage files)