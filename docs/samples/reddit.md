## Using the Reddit sample bundle

The reddit-message-read example bundle in `samples/reddit-msg-read` demonstrates
the ability to read recent posts from a subreddit (in this case `r/skate702`)

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A Reddit Application (Should be of type script for own purpose)

!!! NOTE

    If you don't have such an application yet, you can get one
    [here](https://www.reddit.com/prefs/apps).

### Configure the Reddit sample bundle

1. In NodeCG, create a new Reddit service instance.

2. Enter your applications ID and secret and your own username and password. The
   entered username and password must be for the user who registered the
   application:

    ```json
    {
        "clientId": "Your client Id (This is displayed right below the application name)",
        "clientSecret": "Your client secret",
        "username": "Your username",
        "password": "Your password"
    }
    ```

    After entering it, click save.

3. Set the sample's (`reddit-msg-read`) dependency to be the newly created
   service instance (of type `reddit`).

4. Check the NodeCG logs:

    You should see the recent posts in `r/skate702`
