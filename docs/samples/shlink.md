## Using the Shlink sample bundle

The Shlink example bundle in `samples/shlink-list-short-urls` demonstrates the
ability to control a [Shlink](https://shlink.io/) server by getting the amount
of short URLs configured on the server. Here is a guide on how to get it
working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   [Shlink server and valid API key / token for it](https://shlink.io/documentation/install-docker-image/)

### Configure the Shlink sample bundle

1. In NodeCG, create a new Shlink service instance using the left upper menu.
2. Enter the configuration for Shlink.

    The created instance should be automatically selected, if not, select it in
    the upper left menu. Enter the connection information for the Shlink server
    in monaco (the text-editor on the right) in this format:

    ```json
    {
        "url": "https://example.com",
        "apiKey": "1ae89449-f8d2-4b44-baf7-dd7eb0b05017"
    }
    ```

    After entering it, click save.

3. Set the created Shlink service instance to the service dependency of the
   `shlink-list-short-urls` bundle.

    Select the `shlink-list-short-urls` bundle and the Shlink service in the
    left bottom menu. Then select the service instance that should be used by
    the `shlink-list-short-urls` bundle (in this case the name of the previously
    created Shlink instance).

4. Check the NodeCG logs

    You should see an error or a success message and the amount of configured
    short URLs on the Shlink server.

    _Note:_ When listing short URLs — like this sample does — be aware that the
    amount of short URLs might be limited by the
    [API key role](https://shlink.io/documentation/api-docs/api-key-roles/).
