# Sports Plus+ Android app

This project turns the Sports Plus+ web app into an installable Android app (an APK). GitHub builds it for you, so you do not need Android Studio.

## Build the APK
1. On GitHub, create a new repository (for example `sports-plus-app`).
2. Upload everything from this folder, including the `.github` folder.
   If the `.github` folder did not upload, use Add file > Create new file, type `.github/workflows/build-apk.yml` as the name, and paste in the contents of `build-apk.yml` from this folder.
3. Open the Actions tab. The "Build Android APK" job starts by itself (or tap Run workflow). It takes about 5 to 10 minutes.
4. When it shows a green tick, open the run and download `sports-plus-apk` from Artifacts. Unzip it to get `app-debug.apk`.

## Install on a phone
Send `app-debug.apk` to the phone (WhatsApp as a document, Google Drive, or a cable). Open it and allow "install unknown apps" when asked. Play Protect may warn about an app it does not know; choose to install anyway.

## Updating the app
Upload the new `www/index.html` to the repository. GitHub builds a new APK. Install it over the old one: the data stays, because every build is signed with the same key (`debug.keystore`). Do not delete or replace that file.

## Data
Scores and registrations are saved inside the app on each phone. Uninstalling the app deletes them, so copy the Backup box (Tables or Standings tab) first. To move data from the web version, copy its Backup box and paste it into the app's Backup box, then tap Restore.
