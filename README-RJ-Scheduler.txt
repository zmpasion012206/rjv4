RJ-Scheduler - Complete project v2.9 (versionCode 11)
=================================================

WHAT'S NEW
- Overnight shifts allowed (e.g. 11:00 PM -> 7:00 AM = 8 hrs, shown as "(next day)")
- App logo in the top-left corner of the Schedule screen
- Reliable automatic 11:59 PM sending (SendJob waits for internet, retries)
- SendReceiver + BootReceiver included
- Build signs the APK with YOUR key automatically once the 4 key secrets are set up

WHAT'S IN THIS ZIP (same layout as your repository)
  .github/workflows/build.yml                  -> goes at the TOP of the repo
  RJ-Scheduler/app/build.gradle                -> version 5 (2.3)
  RJ-Scheduler/app/src/main/AndroidManifest.xml
  RJ-Scheduler/app/src/main/assets/index.html  -> the app screens
  RJ-Scheduler/app/src/main/java/com/rj/scheduler/*.java (5 files)

HOW TO UPLOAD
1. Unzip this file on your PC.
2. Open https://github.com/imobile01/RJ_scheduler (the TOP of the repo, not inside a folder).
3. Add file -> Upload files.
4. Open the unzipped folder and drag BOTH folders  ".github"  and  "RJ-Scheduler"
   into the GitHub upload box at the same time. (Don't upload this text file.)
5. Click "Commit changes". GitHub replaces the matching files.
6. Go to Actions. The build starts by itself (about 5-8 minutes).
7. When it's green, open the run -> Artifacts -> RJ-Scheduler-apk -> download -> unzip.

WHICH APK YOU GET
- RJ-Scheduler.apk           = signed with YOUR key (key secrets are set up). Updates keep data.
- RJ-Scheduler-TEMP-KEY.apk  = key secrets NOT set up yet. Works on a fresh install only;
                               it will NOT install over an app signed with your own key.

KEY SECRETS (Settings -> Secrets and variables -> Actions)
  KEYSTORE_BASE64, KEYSTORE_PASSWORD, KEY_ALIAS, KEY_PASSWORD

NEXT TIME
- For a new version, change versionCode to a higher number (6, 7, ...) in
  RJ-Scheduler/app/build.gradle so phones accept it as an update.

THIS ZIP IS THE COMPLETE PROJECT
- Use it to set up a brand-new repository, or to replace everything in your current one.
- To start fresh: create a new repository on GitHub, then upload BOTH folders
  (".github" and "RJ-Scheduler") at the top of the repo, then add the 4 key secrets.
- To build on your PC instead: open the "RJ-Scheduler" folder in Android Studio and
  choose Build > Build App Bundle(s) / APK(s) > Build APK(s).
