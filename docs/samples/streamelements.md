## Using the StreamElements sample bundle

The StreamElements-events example bundle in `samples/streamelements-events`
demonstrates the ability to react to events like donations and subs. Here is a
guide to how to get it working.

### Prerequisites

You will need a working `nodecg-io` installation. If you have non yet take a
look at [installation guide](../getting_started/install.md). You may need to
install this bundle, so take a look at the
[“Try an included sample”](../getting_started/try_example_bundle.md)-Guide. It
will also tell you how to log in and how to use the GUI.

**You also need:**

-   A StreamElements account

### Getting JWT Token

To use the StreamElements service you need a JWT Token that gives it access to
your account.

To get it go to <https://streamelements.com/dashboard/account/channels>, login,
click on `Show Secrets` and copy it.

### Configure the StreamElements sample bundle

1. In NodeCG, create a new StreamElements service instance using the left upper
   menu.

2. Enter credentials for StreamElements.

    The created instance should be automatically selected, if not select it in
    the upper left menu. Enter your JWT Token in monaco (the text-editor on the
    right) in this format:

    ```json
    {
        "jwtToken": "<your JWT Token>"
    }
    ```

    After entering it, click save.

3. Set the created StreamElements service instance to the service dependency of
   the streamelements-events bundle.

    Select the streamelements-events bundle and the StreamElements service in
    the left bottom menu. Then select the service instance that should be used
    by the streamelements-events bundle (in this case the name of the previously
    created streamelements-events instance).

4. Check the nodecg logs

    You should see an error or a success message and a log message for each
    event of your channel like subs, follows, cheers, raids and so on.
