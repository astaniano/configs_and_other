First download adb. Official website says:  
`adb` is included in the Android SDK Platform Tools package. Download this package with the SDK Manager, which installs it at android_sdk/platform-tools/. 
If you want the standalone Android SDK Platform Tools package, download it here (https://developer.android.com/tools/releases/platform-tools)

So download android-platform-tools
```bash
unzip android-platform-tools
cd android-platform-tools
```
inside you'll find a binary executable `adb`

Connect your android via usb cable  
On your android phone go to Settings > About phone > Software information > Build number (tap 7 times on Build number)  
Go back to Settings and see that `Developer options` appeared  
Go to `Developer options` and enable USB debugging

Then run
```bash
./adb devices
```
and on your phone confirm the connection

To get into the device file system now you can run
```bash
./adb shell
```
For get/push data into/out the device:
```bash
./adb pull /storage/self/primary/DCIM/Camera/some.jpg <local_path>
./adb push <local_path> <device_path>
```

To kill adb server on the laptop
```bash
./adb kill-server
```

maybe a useful article:
https://medium.com/@jhaveri_jeet/mastering-adb-the-ultimate-guide-to-android-debug-bridge-commands-c1dabac06739
