# Screen Fill

Android app (accessibility service + floating "Fill" button). Tap the button in
another app: it finds the input box, takes the longest text above it, copies it
to the clipboard and types it into the box.

## Get the APK (no Android Studio needed)

1. Create a new GitHub repo and upload everything in this folder (keep the
   `.github` folder).
2. Open the repo's **Actions** tab -> **Build APK** -> wait for the green check
   (about 3-5 minutes). It also runs on every push.
3. Open the finished run, download the **ScreenFill-apk** artifact (a zip),
   unzip it to get `app-debug.apk`.

Or open this folder in Android Studio and run **Build > Build APK(s)**.

## Install and set up on the phone

1. Install `app-debug.apk` (allow "install unknown apps" for your browser/files app).
2. Open **Screen Fill** -> **Open Accessibility settings** -> Installed/Downloaded
   apps -> **Screen Fill** -> turn on.
   - Android 13+: if the switch is greyed out, go to Settings > Apps > Screen
     Fill > three-dot menu > **Allow restricted settings**, then try again.
3. A round **Fill** button floats over every app. Drag it anywhere.
4. Open the app you're testing and tap **Fill**.

## Notes

- Picks the topmost input box and the longest text above it.
- Apps that block accessibility reading (secure screens) won't work.
