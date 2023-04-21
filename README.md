## TWRP device tree for LG G6 (T-Mobile H872)

Add to `.repo/local_manifests/h872.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<remote name="LG-G6" fetch="https://github.com/LG-G6"/>
	<project path="device/lge/h872" name="twrp_device_lge_h872" remote="LG-G6" revision="android-7.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```
. build/envsetup.sh
lunch omni_h872-eng
mka recoveryimage
```

Kernel sources are available at: https://github.com/LineageOS/android_kernel_lge_msm8996

