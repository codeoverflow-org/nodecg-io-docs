## Using the YouTube sample bundle

The YouTube bundle in `samples/youtube-playlist` demonstrates the ability of
getting information of a playlist. Here is a guide to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   Google cloud API OAuth access (client ID, client Secret)
-   Grant `YouTube Data API v3` access at the project's dashboard.
    -   Shortcut URL:
        `https://console.developers.google.com/apis/library/youtube.googleapis.com?project=<project-id>`.

!!! NOTE

    If you don't have such a key yet, you can generate them like
    [this](https://developers.google.com/identity/protocols/oauth2/web-server#creatingcred).
    As redirect URI add:

    <http://localhost:9090/nodecg-io-googleapis/oauth2callback>

### Configure the YouTube sample bundle

1.  In NodeCG, create a new googleapis service instance.

2.  Enter your YouTube OAuth credentials:

    ```json
    {
        "clientID": "<clientID>",
        "clientSecret": "<clientSecret>",
        "scopes": ["https://www.googleapis.com/auth/youtube"]
    }
    ```

    After entering it, click save.

    !!! NOTE

        You can add multiple scopes if the googleapis instance is used for
        multiple bundles.

3.  Set the sample's (`youtube-playlist`) dependency to be the newly created
    service instance (of type `googleapis`).

4.  Check the NodeCG logs:

    You should see an error or a success message that is hardcoded in
    `samples/youtube-playlist/extension/index.ts`.
