## Using the MQTT-client sample bundle

The MQTT-client sample bundle in `samples/mqtt-client` shows how to connect to
an MQTT server. This client is based on the
[MQTT.js](https://github.com/mqttjs/MQTT.js) package.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   MQTT-server

### Configure the MQTT-client sample bundle

1. In NodeCG, create a new mqtt-client service instance using the left upper
   menu.

2. Enter the connection parameters of the mqtt server. The URL should be in
   following the pattern `<protocol>://<address>:<port>`. Allowed protocols are:
   `mqtt`, `mqtts`, `tcp`, `tls`, `ws`, `wss`.

    In case your server needs authentication, set the `username` and `password`
    fields otherwise remove them from the configuration. The created instance
    should be automatically selected, if not select it in the upper left menu.
    Enter your configuration in monaco (the text-editor on the right) in this
    format:

    ```json
    {
        "address": "mqtt://localhost",
        "topics": ["sample/topic", "diffrent/topic2"],
        "username": "yourUser",
        "password": "yourPassword"
    }
    ```

    After entering it, click save.

3. Set the created mqtt-client service instance to the service dependency of the
   mqtt-client bundle.
4. The console should display if the connection was successfully established and
   should show inbound messages on the subscribed topic.
