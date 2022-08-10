### keystone

- jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore ottpocket.keystore app-release-unsigned.apk ottpocket
- zipalign -v 4 app-release-unsigned.apk ottpocket.apk
- keytool -list -v -keystore ottpocket.keystore

### aab

java -jar bundletool-all-1.8.0.jar build-apks --mode universal --bundle=app-release.aab --output=app.apks --ks=ottpocket.keystore --ks-key-alias=ottpocket

### android

```java
<queries>
    <package android:name="com.tencent.mm" />
</queries>
```

### Sign apk

jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore ottpocket.keystore app-release-unsigned.apk ottpocket

zipalign -v 4 app-release-unsigned.apk ottpocket.apk

### IOS 打包

sudo chmod -R 777 ./platforms/ios

sudo ionic cordova build ios

sudo chmod -R 777 ./ng9

sudo chown -R $USER:$GROUP ~/Library/Preferences/insight-nodejs
