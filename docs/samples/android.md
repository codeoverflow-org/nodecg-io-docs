## Using the Android sample bundle

The Android example bundle in `samples/android` shows how to connect to an
Android device and turn on WLAN.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

1. Clone [this](https://github.com/noeppi-noeppi/nodecg-io-android) Git
   Repository
2. Run `gradlew build` (on Windows) or `./gradlew build` (on Linux) inside the
   cloned repository.
3. There will be an apk file generated in
   `app/build/outputs/apk/debug/app-debug.apk`. Install it on the Android
   device.
4. Launch the app. You'll be asked to grant the system alert window permission.
   This is required because the app will do its work in the background. However,
   occasionally when user interaction is required, it needs to launch an
   activity without the user pressing the app icon in the launcher.
5. Install the android developer tools and make sure you have the `adb` command
   in your `PATH`
6. Enable developer options on you device and enable USB debugging there. See
   [here](https://developer.android.com/studio/debug/dev-options).
7. Run `adb start-server`
8. Connect your device via USB. You'll be prompted whether you want to allow USB
   debugging. Press `Allow`.
9. Run `adb device -l`. The output might look like this:

    ```log
    ########               device usb:2-1.7 product:######## model:######## device:######## transport_id:2
    ```

    The hexadecimal number in the first column is your device ID. You'll need
    this later.

10. In NodeCG, create a new android service instance using the left upper menu.
11. Enter the following:

    ```json
    {
        "device": "device_id"
    }
    ```

    Replace `device_id` with your device ID.

12. Set the created android service instance to the service dependency of the
    android sample bundle.  
    Select the android bundle and the android service in the left bottom menu.
    Then select the service instance that should be used by the android sample
    bundle (in this case the name of the previously created android instance).
13. You should see that WLAN is now activated on your device.
