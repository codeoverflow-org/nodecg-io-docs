## Using the Shlink sample bundle

The Shlink example bundle in `samples/shlink-list-short-urls` demonstrates the ability to control a [Shlink](https://shlink.io/) server by getting the amount of short urls configured on the server. Here is a guide on how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   [Shlink server and valid API key / token for it](https://shlink.io/documentation/install-docker-image/)

### Configure the Shlink sample bundle

1. Start nodecg with nodecg-io installed. The shlink-list-short-urls bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new Shlink service instance using the left upper menu.

5. Enter the configuration for Shlink.

    The created instance should be automatically selected, if not, select it in the upper left menu. Enter the connection information for the Shlink server in monaco (the text-editor on the right) in this format:

    ```json
    {
        "url": "https://example.com",
        "apiKey": "1ae89449-f8d2-4b44-baf7-dd7eb0b05017"
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created Shlink service instance to the service dependency of the shlink-list-short-urls bundle.

    Select the shlink-list-short-urls bundle and the Shlink service in the left bottom menu and then select the service instance that should be used by the shlink-list-short-urls bundle (in this case the name of the previously created Shlink instance).

7. Check the nodecg logs

    You should see an error or a success message and the amount of configured short urls on the Shlink server.

    _Note:_ When listing short urls - like this sample does - be aware that the amount of short urls might be limited by the [API key role](https://shlink.io/documentation/api-docs/api-key-roles/).
