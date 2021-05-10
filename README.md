Install from TWRP-Recovery over ADB:

adb shell reboot recovery

adb shell "mount -o rw /system"

adb push "bootanimation.zip" /sdcard/bootanimation.zip

adb shell "mv /system/media/bootanimation.zip /system/media/bootanimation.old"

adb shell "rm /system/media/bootanimation.zip"

adb shell "cp /sdcard/bootanimation.zip /system/media/bootanimation.zip"

adb shell "chmod 644 /system/media/bootanimation.zip"



If you have some magisk modules active check the file in the directory:

/data/adb/modules/"your module"/system/media/bootanimation.zip

and

/system/media/bootanimation.zip

you need to replace both zip-files in order to get the custom boot animation to work again.
