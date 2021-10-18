## Using the Discord RPC sample bundle

The discord-rpc example bundle in `samples/discord-rpc` demonstrates the ability to access a locally running discord client. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A discord application with permissions `indentify` and `rpc`

_Note:_ If you don't have an application yet, you can create one [here](https://discord.com/developers/applications)

### Configure the Discord RPC sample bundle

1. Start nodecg with nodecg-io installed. The discord-rpc bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new discord-rpc service instance using the left upper menu.

5. Enter required information.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your information in monaco (the text-editor on the right) in this format:

    ```json
    {
        "clientId": "your client id",
        "clientSecret": "your client secret"
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created discord-rpc service instance to the service dependency of the discord-rpc bundle.

    Select the discord-rpc bundle and the discord-rpc service in the left bottom menu and then select the service instance that should be used by the discord-rpc sample bundle (in this case the name of the previously created discord-rpc instance).

7. Check the nodecg logs

    You should see an error or a success message displaying your discord username.
