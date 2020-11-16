## Using the serial sample bundle

The serial example bundle in `samples/serial` demonstrates the ability to exchange data with a device that is connected via serial. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   An Arduino or any other microcontroller development board that can send and receive data via serial.

### Configure the serial sample bundle

1. Load a simple serial echo sketch on your microcontroller. You can find a working arduino sketch at the end of this article.

2. Start nodecg with nodecg-io installed. The serial bundle is currently part of it so it should also be loaded. Make shure the device is already connected. Otherwise you wont be able to see the device.

3. Go to the `nodecg-io` tab in the nodecg dashboard.

4. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

5. Create a new serial service instance using the left upper menu.

6. Enter the information of your device.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter the com port or other identifying information in one of these formats:

    ```json
    {
        "device": {
          "port": "COM1"
        }
    }
    ```

    ```json
    {
      "device": {
        "pnpId": "usb-Arduino__www.arduino.cc__0043_75835343030351E0D171-if00"
      }
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.
    _Note:_ If you want to list all connected devices you can open a terminal in `nodecg-io-serial` and run `npm run list`.
    _Note:_ If you are using multiple devices you might want to use the pnpId, since ports can change between reboots!

7. Set the created serial service instance to the service dependency of the serial bundle.

    Select the serial bundle and the serial service in the left bottom menu and then select the service instance that should be used by the serial bundle (in this case the name of the previously created serial instance).

8. Check the nodecg logs

    You should see an error or a success message and nodecg-io will send ping to the microcontroller every 10 seconds. The arduino device will respond with pong. You should see the pong message displayed in the log.

    If you see an error or nothing at all, try making sure your microcontroller is plugged in and recognized correctly. Then restart nodecg, so the service is cleanly restarted. 

### Sample arduino sketch

```cpp
String inputString = "";
boolean stringComplete = false; 

void setup() {
    Serial.begin(9600);
}

// the loop routine runs over and over again forever
void loop() {
    while (Serial.available()) {
        char inChar = (char)Serial.read();
        inputString += inChar;
        if (inChar == '\n') {
            stringComplete = true;
        }
    }
    if (stringComplete) {
        Serial.println("pong");
        stringComplete = false;
    }
    delay(1);        // delay in between reads for stability
}
```
