## Using the serial sample bundle

The serial example bundle in `samples/serial` demonstrates the ability to
exchange data with a device that is connected via serial. Here is a guide to how
to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   An Arduino or any other microcontroller development board that can send and
    receive data via serial.

### Configure the serial sample bundle

1. In NodeCG, create a new serial service instance.

2. Enter the information of your device:

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

    _Note:_ If you want to list all connected devices you can open a terminal in
    `nodecg-io-serial` and run `npm run list`. _Note:_ If you are using multiple
    devices you might want to use the `pnpId`, since ports can change between
    reboots!

3. Set the sample's (`serial`) dependency to be the newly created service
   instance (of type `serial`).

4. Check the NodeCG logs:

    You should see an error or a success message and nodecg-io will send ping to
    the microcontroller every 10 seconds. The Arduino device will respond with
    pong. You should see the pong message displayed in the log.

    If you see an error or nothing at all, try making sure your microcontroller
    is plugged in and recognized correctly. Then restart NodeCG, so the service
    is cleanly restarted.

### Sample Arduino sketch

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
