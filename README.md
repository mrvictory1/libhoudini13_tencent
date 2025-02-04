# libhoudini13_tencent
libhoudini.so + libnb.so extracted from [Tencent's AoW emulator](sj.qq.com). libnb.so library allows libhoudini to function on AMD processors. libhoudini version: `13.0.1_z.Tencent_AoW_Com2.5b RELEASE` Usage instructions for Waydroid:
1. Use [worstperson/waydroid_script](https://github.com/worstperson/waydroid_script) to install libhoudini for Android 13, the script will set up the necessary workarounds to use libhoudini.
2. In `/var/lib/waydroid/waydroid_base.prop` set `ro.dalvik.vm.native.bridge` to `libnb.so`
3. Copy contents of system/ in this repository to `/var/lib/waydroid/overlay/system` overwriting existing files.
In my testing on AMD CPU + AMD GPU and Mesa 24.2.8, any app that tries to interact with mesa crashes with the below error message therefore it is not possible to play any games.
```
EGL-MAIN: failed to get driver name for fd -1
EGL-MAIN: MESA-LOADER: failed to retrieve device information
```
