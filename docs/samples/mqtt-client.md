## Using the MQTT-client sample bundle

The MQTT-client sample bundle in `samples/mqtt-client` shows how to connect to an MQTT server. This client is based on the [MQTT.js](https://github.com/mqttjs/MQTT.js) package.

### Prerequisites

- Working NodeCG & nodecg-io installation
- MQTT-server

### Configure the MQTT-client sample bundle

1. Start nodecg with nodecg-io installed. The mqtt-client bundle is currently part of it, so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new mqtt-client service instance using the left upper menu.

5. Enter the connection parameters of the mqtt server. The URL should be in following the pattern `<protocol>://<address>:<port>`. Allowed protcols are: `mqtt`, `mqtts`, `tcp`, `tls`, `ws`, `wss`

    In case your server needs authentification set the `username` and `password` fields otherwise remove them from the configuration.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your configuration in monaco (the text-editor on the right) in this format:
    
    ```json
     {
        "address": "mqtt://localhost",
        "topics": [
            "sample/topic",
            "diffrent/topic2"
        ],
        "username": "yourUser",
        "password": "yourPassword"
     }
    ```

    After entering it, click save.

6. Set the created mqtt-client service instance to the service dependency of the mqtt-client bundle.

7. The console should display if the connction was successfully established and should show inbound messages on the subscribed topic.
