## Using the gsheets sample bundle

The gsheets bundle in `samples/gsheets` demonstrates the ability of retrieving
all rows where column A is filled. Here is a guide to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   Google cloud API OAuth access (client ID, client Secret)
-   Grant `Google Sheets API v4` access at the project's dashboard.
    -   Shortcut URL:
        <https://console.developers.google.com/apis/library/sheets.googleapis.com?project=<project-id>>

_Note:_ If you don't have such a key yet, you can generate them like
[this](https://developers.google.com/identity/protocols/oauth2/web-server#creatingcred).
As the redirect URI add
<http://localhost:9090/nodecg-io-googleapis/oauth2callback>.

### Configure the gsheets sample bundle

1. In NodeCG, create a new googleapis service instance.
2. Enter the credentials for googleapis:

    ```json
    {
        "clientID": "<clientID>",
        "clientSecret": "<clientSecret>",
        "scopes": ["https://www.googleapis.com/auth/spreadsheets"]
    }
    ```

    After entering it, click save.

    _Note:_ You can add multiple scopes if the googleapis instance is used for
    multiple bundles.

3. Set the sample's (`gsheets`) dependency to be the newly created service
   instance (of type `googleapis`).
4. Check the NodeCG logs:

    You should see an error or a success message that is hardcoded in
    `samples/gsheets/extension/index.ts`.
