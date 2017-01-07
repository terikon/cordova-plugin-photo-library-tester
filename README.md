Tester app for [cordova-plugin-photo-library](https://github.com/terikon/cordova-plugin-photo-library).

That's how tests look like in the app:

<img src="https://terikon.github.io/cordova-plugin-photo-library-tester/images/screenshot-AutoTests.png" width="256" />
<img src="https://terikon.github.io/cordova-plugin-photo-library-tester/images/screenshot-ManualTests.png" width="256" />

# Setting up

    npm run prepare

Add files from test-images folder to image library of the device.

# Running

## Android

    npm run android-run-emulator

Auto tests will fail if permission for storage not granted. First, go to Manual Tests>requestAuthorization test, that will ask for access authorization.

## iOS

    npm run ios-run-device

## Browser

    npm run browser-run

Select test-images folder when asked by the app.

# Workflow for modifying tests

To perform tests before pushing changes to repository, do this:

    cordova plugin remove cordova-plugin-photo-library cordova-plugin-photo-library-tests
    cordova plugin add /local/path/cordova-plugin-photo-library /local/path/cordova-plugin-photo-library/tests --link

Each time refresh needed, run

For browser:

    npm run browser-refresh-plugins-and-run

For android:

    cordova platform remove android
    cordova platform add android
