## Using the telegram sample bundle

The telegram sample bundle in `samples/telegram-bot` shows how to create a simple command.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A telegram bot API token. You can create your bot [here](https://t.me/botfather).

### Configure the telegram sample bundle

1. Start nodecg with nodecg-io installed. The telegram bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new telegram service instance using the left upper menu.

5. Enter the token and set polling to true.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your host and port in monaco (the text-editor on the right) in this format:

    ```json
    {
        "token": "[TOKEN]",
        "polling": true
    }
    ```

    After entering it, click save.

6. Set the created telegram service instance to the service dependency of the telegram bundle.

7. You can send "/test" to your bot and it should respond with two messages.
