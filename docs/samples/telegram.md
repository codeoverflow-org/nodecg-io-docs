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

1. Create a new telegram service instance.

2. Enter the token and set polling to true:

    ```json
    {
        "token": "[TOKEN]",
        "polling": true
    }
    ```

    After entering it, click save.

3. Set the sample's (`telegram-bot`) dependency to be the newly created service
   instance (of type `telegram`).

4. You can send `/test` to your bot, and it should respond with two messages.
