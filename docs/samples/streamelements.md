## Using the SteamElements sample bundle

The streamelements-events example bundle in `samples/streamelements-events` demonstrates the ability to react to events like donations and subs. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A StreamElements account

### Getting JWT Token

To use the StreamElements service you need a JWT Token that gives it access to your account.

To get it goto https://streamelements.com/dashboard/account/channels, login, click on `Show Secrets` and copy it.

### Configure the SteamElements sample bundle

1. Start nodecg with nodecg-io installed. The streamelements-events bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new StreamElements service instance using the left upper menu.

5. Enter credentials for StreamElements.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your JWT Token in monaco (the texteditor on the right) in this format:

    ```json
    {
        "jwtToken": "<your JWT Token>"
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.

6. Set the created StreamElements service instance to the service dependency of the streamelements-events bundle.

    Select the streamelements-events bundle and the StreamElements service in the left bottom menu and then select the service instance that should be used by the streamelements-events bundle (in this case the name of the previously created streamelements-events instance).

7. Check the nodecg logs

    You should see an error or a success message and a log message for each event of your channel like subs, follows, cheers, raids and so on.
