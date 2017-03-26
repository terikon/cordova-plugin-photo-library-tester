Tester app for [cordova-plugin-photo-library](https://github.com/terikon/cordova-plugin-photo-library).

That's how tests look like in the app:

<img src="https://terikon.github.io/photo-library-tester/images/screenshot-AutoTests.png" width="256" />
<img src="https://terikon.github.io/photo-library-tester/images/screenshot-ManualTests.png" width="256" />

# Setting up

    npm run prepare

Add files from test-images folder to image library of the device.

On android, use one of these:

    npm run copy-test-images:android:emulator
    npm run copy-test-images:android:device

On iOS, go to iTunes, and sync test-images folder with device, or use:

    npm run copy-test-images:ios:simulator

# Running

## Android

Run one of these:

    npm run run:android:emulator
    npm run run:android:device

Auto tests will fail if permission for storage not granted. First, go to Manual Tests>requestAuthorization test, that will ask for access authorization.

## iOS

    npm run run:ios:device

## Browser

    npm run run:browser

Select test-images folder when asked by the app.

# Workflow for modifying tests

To perform tests before pushing changes to repository, do this:

    cordova plugin remove cordova-plugin-photo-library cordova-plugin-photo-library-tests
    cordova plugin add /local/path/cordova-plugin-photo-library /local/path/cordova-plugin-photo-library/tests --link

Each time refresh needed, run

For browser:

    npm run refresh-plugins:run:browser

For android:

    cordova platform remove android
    cordova platform add android
