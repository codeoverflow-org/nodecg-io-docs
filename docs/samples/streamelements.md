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

1. In NodeCG, create a new StreamElements service instance.

2. Enter the JWT Token for StreamElements:

    ```json
    {
        "jwtToken": "<your JWT Token>"
    }
    ```

    After entering it, click save.

3. Set the sample's (`streamelements-events`) dependency to be the newly created
   service instance (of type `streamelements`).

4. Check the NodeCG logs:

    You should see an error or a success message and a log message for each
    event of your channel like subs, follows, cheers, raids and so on.
