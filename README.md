Tester add for [cordova-plugin-photo-library](https://github.com/terikon/cordova-plugin-photo-library).

# Setting up

    cordova prepare

Add files from test-images folder to image library of the device.

# Running

## Android

    npm run android-run-emulator

## Browser

    npm run browser-run

Select test-images folder when asked by the app.

# Workflow for modifying tests

To perform tests before pushing changes to repository, do this:

    cordova plugin remove cordova-plugin-photo-library cordova-plugin-photo-library-tests
    cordova plugin add /local/path/cordova-plugin-photo-library /local/path/cordova-plugin-photo-library/tests --link

Each time refresh needed, run

    npm run browser-refresh-plugins-and-run