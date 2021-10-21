## Using the telegram sample bundle

The telegram sample bundle in `samples/telegram-bot` shows how to create a
simple command.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A telegram-bot API token. You can create your bot
    [here](https://t.me/botfather).

### Configure the telegram sample bundle

1. Create a new telegram service instance using the left upper menu.

2. Enter the token and set polling to true.

    The created instance should be automatically selected, if not select it in
    the upper left menu. Enter your host and port in monaco (the text-editor on
    the right) in this format:

    ```json
    {
        "token": "[TOKEN]",
        "polling": true
    }
    ```

    After entering it, click save.

3. Set the created telegram service instance to the service dependency of the
   telegram bundle.

4. You can send `/test` to your bot, and it should respond with two messages.
