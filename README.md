# Convert Android Pixel 3a to Ubuntu Touch - Pixel 3a

This repository provides a step-by-step guide to help you convert your Android Pixel 3a device to Ubuntu Touch. Ubuntu Touch is a mobile operating system based on Ubuntu that offers a unique and open-source experience for smartphones and tablets.

* Escape Big Tech's Control: Say goodbye to invasive data collection and regain control over your personal information.
* Privacy-Centric Ubuntu Touch: Experience the freedom of Ubuntu Touch while safeguarding your digital privacy.
* Step-by-Step Conversion Guide: Our detailed guide walks you through the process of unlocking, flashing, and setting up Ubuntu Touch on your Pixel 3a.


## Why Ubuntu Touch?

* Privacy: Ubuntu Touch prioritizes user privacy by minimizing data collection and offering comprehensive privacy controls.

* Customization: Tailor your mobile experience to your preferences with a variety of customization options, from theming to app layouts.

* Security: Benefit from regular security updates and a secure architecture that puts you in control of your device's data.

* Open Source: Ubuntu Touch is built on open-source principles, giving you the freedom to explore, modify, and contribute to the operating system.

Prerequisites
-------------

Before you begin, make sure you have the following:

* A Google Pixel 3a device (Make sure you have backed up all your important data.)
* A computer running Linux (Ubuntu recommended)
* USB cable for connecting your device to the computer
* Basic knowledge of the command line

Steps
-------------

### 1\. Unlock Bootloader

1. Enable Developer Options on your Pixel 3a: Go to **Settings > About phone > tap Build number 7 times**.

2. Enable USB Debugging and OEM Unlock: In Developer Options, enable **USB Debugging** and **OEM Unlocking**.

3. Connect your Pixel 3a to the computer via USB.

4. Open a terminal on your computer and enter the following command to reboot into the bootloader:

    `adb reboot bootloader`

5. Unlock the bootloader using the following command:

    `fastboot flashing unlock`

    Follow the on-screen instructions on your device to confirm the unlock process.

### 2\. Install Ubuntu Touch

1. Download the latest Ubuntu Touch image for the Pixel 3a from the official UBports website: [UBports Devices page](https://devices.ubuntu-touch.io/device/sargo/).

2. Extract the downloaded image to a convenient location on your computer.

3. Reboot your Pixel 3a into the bootloader again:

    bashCopy code

    `adb reboot bootloader`

4. Flash the Ubuntu Touch image using the following command:

    `fastboot flash system /path/to/ubuntu-touch-image.img`

5. Once the flashing process is complete, reboot your device:

    `fastboot reboot`

### 3\. Initial Setup

1. When your device boots into Ubuntu Touch, follow the on-screen instructions to complete the initial setup.
2. Connect to a Wi-Fi network and sign in with your Ubuntu One account or create a new account.

### 4\. Post-Installation Steps

1. Install Updates: Go to **System Settings > Updates** and check for system updates. Install any available updates to ensure you're running the latest version of Ubuntu Touch.

2. Install Apps: You can browse and install apps from the OpenStore, which is the official app store for Ubuntu Touch. Simply open the OpenStore app from the App Drawer and search for the apps you need.

Disclaimer
-------------

Please note that the process of converting your Pixel 3a to Ubuntu Touch involves unlocking the bootloader and flashing custom software, which can void your warranty and potentially brick your device if not done correctly. Follow the steps carefully and understand the risks before proceeding.
While this repository aims to provide comprehensive and accurate information, please note that the process of transitioning to Ubuntu Touch involves technical steps that can potentially impact your device. Proceed with caution and ensure you fully understand the process before making any changes.

Support
-------

If you encounter any issues during the process, you can seek help from the Ubuntu Touch community through the following channels:

* [UBports Forum](https://forums.ubports.com/)
* [UBports Telegram Group](https://t.me/ubports)
* [UBports Matrix Chat](https://matrix.to/#/#ubports:matrix.org)

Contributing
------------

If you find any errors or improvements to this guide, feel free to open an issue or submit a pull request to this repository.


I found that Google usb driver must be installed on windows 11 <https://developer.android.com/studio/run/win-usb> before connecting device to usb port.

1. complete the setup of the phone WIFI and bare minimum
2. then oem onlock greyed out is enabled and should be toggled

3. adb reboot-bootloader (enters the phone into a state stating that it is locked)

4. Command promont: `fastboot flashing unlock`

```
 OKAY [  0.136s]
 Finished. Total time: 0.138s
```

5. On the device select `Unlock the bootloader'

6. Start the device -> go thru the wizard again -> enable developer mode as well

7. <https://devices.ubuntu-touch.io/device/sargo/>

8. <https://developers.google.com/android/images#sargo> and search for PQ3B.190801.002

```bash
  adb kill-server
 then flash device
 allow adb
```

7. Setup Android device no need for wifi
8. Start the phone About Phone --> Build Number
9. Download Ubuntu touch install  <https://devices.ubuntu-touch.io/device/sargo/>

## References

* [Video](https://www.youtube.com/watch?v=v3nZSKsedr4&ab_channel=Lumpology)


**Happy migrating and exploring the open world of Ubuntu Touch on your Pixel 3a!**
