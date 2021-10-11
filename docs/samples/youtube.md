## Using the youtube sample bundle

The youtube bundle in `samples/youtube-playlist` demonstrates the ability of getting information of a playlist. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   Google cloud API OAuth access (clientID, clientSecret)
-   Grant `YouTube Data API v3` access at the project's dashboard.
    -   Shortcut URL: https://console.developers.google.com/apis/library/youtube.googleapis.com?project=&lt;project-id&gt;

_Note:_ If you don't have such a key yet, you can generate them like [this](https://developers.google.com/identity/protocols/oauth2/web-server#creatingcred). As redirect URI add "http://localhost:9090/nodecg-io-googleapis/oauth2callback".

### Configure the youtube sample bundle

1. Start nodecg with nodecg-io installed. The youtube bundle is currently part of it so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new googleapis service instance using the left upper menu.

5. Enter credentials for googleapis.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your youtube oauth credentials in monaco (the text-editor on the right) in this format:

    ```json
    {
        "clientID": "<clientID>",
        "clientSecret": "<clientSecret>",
        "scopes": ["https://www.googleapis.com/auth/youtube"]
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.  
    _Note:_ You can add multiple scopes if the googleapis instance is used for multiple bundles.

6. Set the created googleapis service instance to the service dependency of the youtube bundle.

    Select the youtube bundle and the googleapis service in the left bottom menu and then select the service instance that should be used by the youtube bundle (in this case the name of the previously created googleapis instance).

7. Check the nodecg logs

    You should see an error or a success message that is hardcoded in `samples/youtube-playlist/extension/index.ts`.
