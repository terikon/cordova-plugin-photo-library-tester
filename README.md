Tester app for [cordova-plugin-photo-library](https://github.com/terikon/cordova-plugin-photo-library).

That's how tests look like in the app:

![Automatic tests](https://terikon.github.io/cordova-plugin-photo-library-tester/images/screenshot-AutoTests.png =256)
![Manual tests](https://terikon.github.io/cordova-plugin-photo-library-tester/images/screenshot-ManualTests.png =256)

# Setting up

    cordova prepare

Add files from test-images folder to image library of the device.

# Running

## Android

    npm run android-run-emulator

Auto tests will fail if permission for storage not granted. First, go to Manual Tests>requestAuthorization test, that will ask for access authorization.

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
