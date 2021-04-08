## Using the Android sample bundle

The Android example bundle in `samples/android` shows how to connect to an android device and turn on WLAN.

1. clone [this](https://github.com/noeppi-noeppi/nodecg-io-android) Git Repository

2. Run `gradlew build` (on Windows) or `./gradlew build` (on linux) inside the cloned repository.

3. There will be an apk file generated in `app/build/outputs/apk/debug/app-debug.apk`. Install it on the device.

4. Launch the app. You'll be asked to grant the system alert window permission. This is required because the app will do its work in the background. However occasionally when user interaction is required, it needs to launch an activity without the user pressing the app icon in the launcher.

5. Install the android developer tools and make sure you have the `adb` command in your `PATH`

6. Enable developer options on you device and enable USB debugging there. See [here](https://developer.android.com/studio/debug/dev-options)

7. Run `adb start-server`

8. Connect your device via USB. You'll be prompted whether you want to allow USB debugging. Press `Allow`

9. Run `adb device -l`. The output might look like this:

   ```
   ########               device usb:2-1.7 product:######## model:######## device:######## transport_id:2
   ```
   
   The hexadecimal number in the first column is your device id. You'll need this later.

10. Start nodecg with nodecg-io installed. The bundle is currently part of it so it should also be loaded.

11. Go to the `nodecg-io` tab in the nodecg dashboard.

12. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

13. Create a new android service instance using the left upper menu.

14. Enter the following

    ```
    {
        "device": "device_id"
    }
    ```

    Replace `device_id` with your device id.

15. Set the created android service instance to the service dependency of the android sample bundle.

    Select the android bundle and the android service in the left bottom menu and then select the service instance that should be used by the android sample bundle (in this case the name of the previously created android instance).

16. You should see that WLAN is now activated on your device.
