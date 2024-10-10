# Android14_to_MacOS_Sequoia15
Instruction how to copy data from Android 14 smartphone to the MacOS Sequoia 15

Devices connected with USB cable.

On the Android 14 smartphone:
1. Unlock Developer options: Go to `Settings` > `About phone` and then tap `Build number` seven times. Enter your password when prompted, and a new Developer options menu will appear in your System settings.
2. Enable USB debugging: Go to `Settings` > `System` > `Developer options` and toggle on `USB debugging`.

On the Macbook:
1. `brew install android-platform-tools`
2. `adb start-server`
3. `adb devices` - you should see Android device
4. `adb shell ls /sdcard/` - you should see the not-only-for-root-user directories. Move your files there if you don't want to deal with root permissions.
5. `adb pull /sdcard/filename /path/to/destination/on/mac` - copy your files!
6. `adb disconnect` - optional
7. `adb kill-server`
