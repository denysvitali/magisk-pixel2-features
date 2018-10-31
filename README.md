# Pixel 2 Features

**Fix for Magisk 17+ work**


**Still in development..., ~~we need libsense.so~~ found it!**
*Requires Magisk v1.4.10+* (for no particular reason)

## Requirements
- Android 8.0+
- arm64 device (yes, N5X, N6P, Pixel 1, Pixel 1 XL are arm64)
- Magisk Root
- Time

## Current problem

```
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader: Failed to stop and unload the sound model.
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader: bnz: SoundTriggerManager.stopRecognition
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at bny.a(PG:24)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at bil.c(PG:3)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at bil.a(PG:35)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at bih.onSharedPreferenceChanged(Unknown Source:2)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.app.SharedPreferencesImpl$EditorImpl.notifyListeners(SharedPreferencesImpl.java:560)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.app.SharedPreferencesImpl$EditorImpl.apply(SharedPreferencesImpl.java:443)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at co.a(PG:3)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.support.v7.preference.Preference.a(PG:11)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.support.v7.preference.Preference.e(PG:5)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.support.v7.preference.TwoStatePreference.g(PG:1)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.support.v7.preference.TwoStatePreference.e(PG:4)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.support.v7.preference.Preference.a(PG:21)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.support.v14.preference.SwitchPreference.a(PG:1)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at mx.onClick(Unknown Source:2)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.view.View.performClick(View.java:6256)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.view.View$PerformClick.run(View.java:24697)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.os.Handler.handleCallback(Handler.java:789)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.os.Handler.dispatchMessage(Handler.java:98)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.os.Looper.loop(Looper.java:164)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at android.app.ActivityThread.main(ActivityThread.java:6541)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at java.lang.reflect.Method.invoke(Native Method)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at com.android.internal.os.Zygote$MethodAndArgsCaller.run(Zygote.java:240)
10-19 17:47:24.442 14814 14814 E SoundTriggerModelLoader:       at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:767)
```

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
