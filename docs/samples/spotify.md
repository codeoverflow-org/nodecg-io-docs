## Using the Spotify sample bundle

The spotify-current-song example bundle in `samples/spotify-current-song`
demonstrates the ability to get the current playing song of a user. Here is a
guide to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A Spotify account and a registered Spotify application and the associated
    client id/client secret.

!!! NOTE

    If you don't have a registered application, yet you can follow
    [this guide](https://developer.spotify.com/documentation/general/guides/authorization/app-settings/).
    As a redirect URL use <http://localhost:9090/nodecg-io-spotify/spotifycallback>.

### Configure the Spotify sample bundle

1.  In NodeCG, create a new Spotify service instance.

2.  Enter your client ID and secret for Spotify:

    ```json
    {
        "scopes": ["user-read-playback-state"],
        "clientId": "0123456789abcdef0123456789abcdef",
        "clientSecret": "0123456789abcdef0123456789abcdef"
    }
    ```

    After entering it, click save.

    !!! NOTE

        This sample requires the `user-read-playback-state` scope, but you
        can require other scopes if you want to use functions that require them. A
        list of all scopes can be found
        [here](https://developer.spotify.com/documentation/general/guides/authorization/scopes/).

3.  Set the sample's (`spotify-current-song`) dependency to be the newly created
    service instance (of type `spotify`).

4.  Check the NodeCG logs:

    You should see an error or a success message and the current playing song
    with names and artists.
