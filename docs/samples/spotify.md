## Using the Spotify sample bundle

The spotify-current-song example bundle in `samples/spotify-current-song` demonstrates the ability to get the current playing song of a user. Here is a guide to how to get it working.

### Prerequisites

-   Working NodeCG & nodecg-io installation
-   A Spotify account and a registered Spotify application and the associated client id/client secret.

_Note:_ If you don't have a registered application, yet you can follow [this guide](https://developer.spotify.com/documentation/general/guides/app-settings/#register-your-app). As a redirect URL use <http://localhost:9090/nodecg-io-spotify/spotifycallback>.

### Configure the Spotify sample bundle

1. Start nodecg with nodecg-io installed. The spotify-current-song bundle is currently part of it, so it should also be loaded.

2. Go to the `nodecg-io` tab in the nodecg dashboard.

3. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

4. Create a new Spotify service instance using the left upper menu.

5. Enter credentials for Spotify.

    The created instance should be automatically selected, if not select it in the upper left menu. Enter your client ID and secret in monaco (the text-editor on the right) in this format:

    ```json
    {
        "scopes": ["user-read-playback-state"],
        "clientId": "0123456789abcdef0123456789abcdef",
        "clientSecret": "0123456789abcdef0123456789abcdef"
    }
    ```

    After entering it, click save.

    _Note:_ If you don't see monaco on the right, try reloading the page.
    _Note:_ This sample requires the `user-read-playback-state` scope, but you can require other scopes if you want to use functions that require them.
    A list of all scopes can be found [here](https://developer.spotify.com/documentation/general/guides/scopes/).

6. Set the created Spotify service instance to the service dependency of the spotify-current-song bundle.

    Select the spotify-current-song bundle and the Spotify service in the left bottom menu and then select the service instance that should be used by the spotify-current-song bundle (in this case the name of the previously created Spotify instance).

7. Check the nodecg logs

    You should see an error or a success message and the current playing song with names and artists.
