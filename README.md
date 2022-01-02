# Magisk On Emulator, Android x86 project

## About
Integrate Magisk root into Nox Player and other Android x86, emulators

<img src="https://github.com/HuskyDG/MagiskOnNox/raw/main/Screenshot%20(3).png" />

## Features

- Bring Magisk / Zygisk to Android x86
- MagiskHide / MagiskDenyList for hiding root
- Magisk / Zygisk modules work properly!

Note: Some features might not work on some emulator, Please read [Emulator that Magisk can work properly](https://github.com/HuskyDG/MagiskOnNox/wiki/Emulator-that-Magisk-can-work-properly) to know which Magisk features doesn't work.

## Requirements
- Android x86 project (BlissOS/PhoenixOS) or Android Emulator (NoxPlayer, LDPlayer, ...): [Emulator that Magisk can work properly](https://github.com/HuskyDG/MagiskOnNox/wiki/Emulator-that-Magisk-can-work-properly).
- Android version: 7.1 ~ 9.0

## Download
Download from [**Releases** tag](https://github.com/HuskyDG/MagiskOnNox/releases/) 


## Installation

### Direct Install

[Video: How to install Magisk and LSPosed on Nox Player emulator]( https://youtu.be/ZtZQPfZjFuU)


Install Magisk into system image, so your system must be able to be mounted as read-write

It's recommended for Android emulator, as you don't have `ramdisk.img`. Also extract `ramdisk.img` through Android emulator environment is very difficult.


1. Go to emulator settings, enable built-in Root and reboot.
-    **Bluestacks:**
    Because Bluestacks emulator doesn't have built-in root option, so you need to use **Bluestacks Tweaker** to install **SuperSU** for root


2. Download and install **Magisk On Nox**. Open and grant root access to **Magisk on Nox** app
3. Do follow the menu to install Magisk. Here are 3 versions of Magisk that you can install: Canary, Alpha and Stable.

4. Go to emulator settings, disable built-in Root and reboot. For Bluestacks, press **UnPatch** button in **Bluestacks Tweaker** to remove **SuperSU**.


### Patch ramdisk image

Recommended if you have `ramdisk.img` or you are using Android x86 project (BlissOS, PhoenixOS)

This guide is quite confusing and may not be for the average user

You must have copy of `ramdisk.img`. It is usually loacted in BlissOS/PhoenixOS folder on volume disk where you installed it.

#### **Patch ramdisk through Android emulator**

-  You can use **Magisk on Nox** to patch `ramdisk.img` of **BlissOS/PhoenixOS** through emulator such as **NoxPlayer, MEmu** and then take new `ramdisk.img`. Replace with magisk patched `ramdisk.img`.

#### **Patch ramdisk through Android x86**

1. Take and transfer it to **Internal Storage** of **BlissOS/PhoenixOS**

-  On **BlissOS/PhoenixOS**, usually you will have `data.img` that will be mounted to `/data` partition when you boot into **BlissOS/PhoenixOS**. 
  
-  If you cannot transfer files between **Windows** and **BlissOS/PhoenixOS**, you can use **[AnyBurn](https://anyburn.com/download.php)** software to read `data.img` (Internal Storage image) to put in or take `ramdisk.img` out while you want to patch through **BlissOS/PhoenixOS**.

2. Boot to **BlissOS/PhoenixOS**. Install **Magisk on Nox** and open, grant root access if you have!

3. If you doesn't have root access, press *ALT+F1* to open root shell, then type this command:
```
/data/data/io.github.huskydg.magiskonnox/magisk/menu
```

4. A menu will be visible, go *Install/update Magisk* > *Magisk build* > *Patch ramdisk image* and enter path to your ramdisk image (ramdisk.img), press Enter and it will patch your **ramdisk.img** and new ramdisk will be saved to `/sdcard/magisk_ramdisk_<random_number>.img`. Press *ALT + F7* to close root shell

5. Now transfer new `ramdisk.img` to Windows disk

6. Boot into **Windows OS**. Open **File Exploerer**, navigate to BlissOS/PhoenixOS folder, make sure you back up old `ramdisk.img` and replace with new patched `ramdisk.img`.

7. Boot to **BlissOS/PhoenixOS** and enjoy **Magisk**.

## Uninstall

- **Magisk on Nox** has option to uninstall Magisk. If you install Magisk into `ramdisk.img`, you cannot uninstall directly, please just replace it with original `ramdisk.img`

## Update

- Since Nox/Emulator doesn't have boot image, you cannot update directly through **Magisk** app, please use **Magisk On Nox** to update it.
- If you install Magisk into `ramdisk.img`, you can use **Update binary** option to update **Magisk** without having to patch `ramdisk.img` again!


## Frequently asked Questions

[Please access this page](https://github.com/HuskyDG/MagiskOnNox/wiki)


## Credits
- [Magisk](https://github.com/topjohnwu/Magisk): The most famous root solution on Android
- [MagiskOnWSA](https://github.com/LSPosed/MagiskOnWSA): For Magisk on WSA script, how to integrate Magisk on Emulator
