# Ubuntu Touch device tree for Xiaomi Mi MIX 3 (perseus)

This is based on Halium 9.0, and uses the mechanism described in [this page](https://github.com/ubports/porting-notes/wiki/GitLab-CI-builds-for-devices-based-on-halium_arm64-(Halium-9)).

You can download the ready-made artifacts from gitlab: take the [latest archive](https://gitlab.com/ubports/community-ports/android9/xiaomi-mi-mix-3/xiaomi-perseus/-/jobs/artifacts/master/download?job=flashable), unpack the `artifacts.zip` file (make sure that all files are created inside a directory called `out/`, then follow the instructions in the [Install](#install) section.

## Pre-requisition:

As this is based on Android 9, it is required to install stock vendor.img from Android 9. You can download from [here](https://github.com/ubports-perseus/ubuntu-touch-perseus/releases/download/v1.0-beta/vendor.zip) or from [Xiaomi Firmware Updater](https://xiaomifirmwareupdater.com/).
DTBO based on LineageOS 16.0 is required to boot the ubuntu touch, get it from [here](https://github.com/ubports-perseus/ubuntu-touch-perseus/releases/download/v1.0-beta/dtbo.img) 

Copy these images to directory `out/` above together with the artifacts.

## Install

```bash
fastboot flash boot out/boot.img
fastboot flash dtbo out/dtbo.img
fastboot flash recovery out/recovery.img
fastboot flash system out/system.img
```

