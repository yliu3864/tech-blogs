**Installation**

1. [Android Studio](https://developer.android.com/studio)
2. [Java v1.8](https://www.oracle.com/ca-en/java/technologies/javase/javase8-archive-downloads.html)

- It has to be v1.8 for ionic development and please make sure you have installed both jdk and jre
- Run `java -version` to check if you have successfully installed the correct version

1. Gradle
2. Ionic CLi
   npm install -g @ionic/cli

### Troubleshoot

Here are some scenarios that you may encounter.

1. **Setting environment variables**

- Window + R → sysdm.cpl → ok → advanced
- Try put %JAVA_HOME% at the beginning in PATH
- Must open command prompt again after updating env variable/PATH value

[https://stackoverflow.com/questions/2380572/java-version-not-working-in-command-prompt](https://stackoverflow.com/questions/2380572/java-version-not-working-in-command-prompt)

2. **ERROR: Installed Build tools revision 31.0.0 is corrupted. Remove and install again using the SDK Manager**

[https://stackoverflow.com/questions/68387270/android-studio-error-installed-build-tools-revision-31-0-0-is-corrupted](https://stackoverflow.com/questions/68387270/android-studio-error-installed-build-tools-revision-31-0-0-is-corrupted)

3. **Can’t see the app data folder**

[https://cybertext.wordpress.com/2012/05/29/cant-see-the-appdata-folder/](https://cybertext.wordpress.com/2012/05/29/cant-see-the-appdata-folder/)

- Go to Explorer.
- Open the **C:** drive.
- Click **View** on the menu bar.
- Click the **Options** icon. (If you click the small arrow below it instead, choose **Change Folder and Search options**).
- Select the **View** tab.
- Under **Files and Folders > Hidden files and folders**, select the option to **Show hidden files, folders and drives**.
- Click **OK**.

4. **APK signing error : Failed to read key from key store**

- Go to <your_app_name>/android.
- On the terminal use `./gradlew signingReport` for Mac OS and `gradlew signingReport` for Windows.
- you must run this command in the android folder
- If using Powershell → ./gradle signingReport
- Check if each element of each task has a Variant, Config, Store, Alias, MD5, SHA1, SHA-256, Valid until. If so you should be good.
- If any of the above are absent then try to regenerate the key store by following the instructions on this page / Or just download from official template and replace the one in .android and in platforms/android/app →  [https://raw.githubusercontent.com/facebook/react-native/master/template/android/app/debug.keystore](https://raw.githubusercontent.com/facebook/react-native/master/template/android/app/debug.keystore)
- Copy the key store file and paste it inside <your_app_name>/android/app.

[https://stackoverflow.com/questions/20453249/apk-signing-error-failed-to-read-key-from-keystore](https://stackoverflow.com/questions/20453249/apk-signing-error-failed-to-read-key-from-keystore)
