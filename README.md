# Pixel 2 Features

**Still in development..., we need libsense.so!**  
*Requires Magisk v1.4.10+* (for no particular reason)

## Requirements
- Android 8.0+
- arm64 device (yes, N5X, N6P, Pixel 1, Pixel 1 XL are arm64)
- Magisk Root
- Time

## Build the module

(Or you know, [click here](https://ded1.denv.it/pixel2-features.zip))

```
zip -x '.git*' -r /tmp/pixel2-features.zip .
```

## Push the module to your device
```
adb push /tmp/pixel2-features.zip /sdcard/
```

## Install module

Open Magisk Manager, install `/sdcard/pixel2-features.zip`, reboot and enjoy.

## Post install setup

You may need to:  
```
# Setup the app (give permissions during the wizard)

adb shell su -c 'am start com.google.intelligence.sense/com.google.intelligence.sense.ambientmusic.AmbientMusicSetupWizardActivity'

# Open the Settings View
adb shell su -c 'am start com.google.intelligence.sense/com.google.intelligence.sense.ambientmusic.AmbientMusicSettingsActivity'
```


## Special thanks to
- Jax (provided like ALL the needed files from his shiny Pixel 2)
- [Kieron Quinn](https://twitter.com/Quinny898) for providing the initial `matcher.leveldb`
- [/u/Devil_Vagina_Magic](https://www.reddit.com/user/Devil_Vagina_Magic) for some needed screens and files
- [/u/Lurking_Grue](https://www.reddit.com/user/Lurking_Grue) for providing some of the files
- [/u/Parmon](https://www.reddit.com/user/Parmon) for providing some of the files
- [Peter Sanchez](https://twitter.com/PeterSanchez) for being helpful :)
- [argraur](https://github.com/argraur) for providing some more files
