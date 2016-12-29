Tester add for [cordova-plugin-photo-library](https://github.com/terikon/cordova-plugin-photo-library).

# Setting up

Add files from test-images folder to image library of the device.

    cordova prepare

To perform tests before pushing changes to repository, temporarly replace following in config.xml:

```xml
<plugin name="cordova-plugin-photo-library" spec="https://github.com/terikon/cordova-plugin-photo-library.git">
<!-- replace with -->
<plugin name="cordova-plugin-photo-library" spec="/local/path/cordova-plugin-photo-library">
```
```xml
<plugin name="cordova-plugin-photo-library-tests" spec="https://github.com/terikon/cordova-plugin-photo-library.git#:/tests" />
<!-- replace with -->
<plugin name="cordova-plugin-photo-library-tests" spec="/local/path/cordova-plugin-photo-library/tests" />
```
And run 

    cordova plugin remove cordova-plugin-photo-library cordova-plugin-photo-library-tests
    cordova plugin add cordova-plugin-photo-library cordova-plugin-photo-library-tests

# Running

## Android

    npm run android-run-emulator

## Browser

    npm run browser-run

Select test-images folder when asked by the app.